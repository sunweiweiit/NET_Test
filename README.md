# NET_Test

protected void Button1_Click(object sender, EventArgs e)  
  
{  
  
           SmtpClient client = new SmtpClient("smtp.qq.com", 587);  
            Random Rdm = new Random();  
            //产生0到100000的随机数  
            int iRdm = Rdm.Next(0000, 99999);  
            MailMessage msg = new MailMessage("A", "B", "验证码", iRdm.ToString());  
            client.UseDefaultCredentials = false;  
            System.Net.NetworkCredential basicAuthenticationInfo =  
             new System.Net.NetworkCredential("A", "C");  
            client.Credentials = basicAuthenticationInfo;  
            client.EnableSsl = true;  
            client.Send(msg);  
  
} 
