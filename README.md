# STUDENT-RECORDS-MANAGEMENT
using System;

using System.Collections.Generic;

using System.ComponentModel;

using System.Data;

using System.Drawing;

using System.Linq;

using System.Text;

using System.Threading.Tasks;

using System.Windows.Forms;

namespace Studnt_Record

{

    public partial class Form1 : Form

    {

        DataTable table = new DataTable("table");

        int index;

        public Form1()

        {

            InitializeComponent();

        }

        private void Form1_Load(object sender, EventArgs e)

        {

            table.Columns.Add("StudentID", Type.GetType("System.Int32"));

            table.Columns.Add("KARL LHESTER HOWARD", Type.GetType("System.Int32"));

            table.Columns.Add("SOLIS", Type.GetType("System.Int32"));

            table.Columns.Add("08-12-02", Type.GetType("System.Int32"));

            table.Columns.Add("20", Type.GetType("System.Int32"));

            table.Columns.Add("MALE", Type.GetType("System.Int32"));

            table.Columns.Add("llanera plaridel", Type.GetType("System.Int32"));

            table.Columns.Add("09564625967", Type.GetType("System.Int32"));

            dataGridView1.DataSource = table;

            MessageBox.Show("Record Inserted");

        }

        private void dataGridView1_CellContentClick(object sender, DataGridViewCellEventArgs e)

        {

            int index;

            index = e.RowIndex;

            DataGridViewRow row = dataGridView1.Rows[index];

            textBox1.Text = row.Cells[0].Value.ToString();

            textBox2.Text = row.Cells[1].Value.ToString();

            textBox3.Text = row.Cells[2].Value.ToString();

            StextBox4.Text = row.Cells[3].Value.ToString();

            textBox5.Text = row.Cells[4].Value.ToString();

            textBox6.Text = row.Cells[5].Value.ToString();

            textBox7.Text = row.Cells[6].Value.ToString();

            textBox8.Text = row.Cells[7].Value.ToString();

        }

        private void button2_Click(object sender, EventArgs e)

        {

            table.Rows.Add(textBox1.Text);

            MessageBox.Show("Record Inserted");

        }

        private void button4_Click(object sender, EventArgs e)

        {

            index = dataGridView1.CurrentCell.RowIndex;

            dataGridView1.Rows.RemoveAt(index);

            MessageBox.Show("Item Removed");

        }

        private void button6_Click(object sender, EventArgs e)

        {

            DataGridViewRow newData = dataGridView1.Rows[index];

            newData.Cells[0].Value = textBox1.Text;

            newData.Cells[1].Value = textBox2.Text;

            newData.Cells[2].Value = textBox3.Text;

            newData.Cells[3].Value = textBox4.Text;

            newData.Cells[4].Value = textBox5.Text;

            newData.Cells[5].Value = textBox6.Text;

            newData.Cells[6].Value = textBox7.Text;

            newData.Cells[7].Value = textBox8.Text;

            MessageBox.Show("Record Updated");

        }

        private void button5_Click(object sender, EventArgs e)

        {

            int SearchID;

            SearchID=int.Parse(textBox1.Text);

            if (SearchID == 1)

            {

                textBox2.Text = "KARL LHESTER HOWARD SOLIS";

                textBox3.Text = "Kahit ano";

                textBox4.Text = "08-12-2002";

                textBox5.Text = "2";

                textBox6.Text = "MALE";

                textBox7.Text = "Nueva Ecija";

                textBox8.Text = "09564625967";

            }

            else

             {

                textBox2.Text = ("No Record");

                textBox3.Text = ("No Record");

                textBox4.Text = ("No Record");

                textBox5.Text = ("No Record");

                textBox6.Text = ("No Record");

                textBox7.Text = ("No Record");

                textBox8.Text = ("No Record");

            }

           

    }

    }

}
