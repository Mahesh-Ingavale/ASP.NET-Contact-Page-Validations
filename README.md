
# ASP.NET-Contact-Page-Validations Textbox, Contact Number, Email Address, Submit Button Validations Included.   
<br />
# Note : Framework doesn't allow more than one form tag on single page. 
<hr />

<div>
    <asp:TextBox ID="txtname" type="text" placeholder="Your Name" class="contact-form" runat="server"></asp:TextBox>
    <asp:RequiredFieldValidator ID="RequiredFieldValidator1" runat="server" ErrorMessage="**Please Enter Your Name**" ControlToValidate="txtname"></asp:RequiredFieldValidator>
</div>

<div>
    <asp:TextBox ID="txtemail" type="email" placeholder="Your Email" class="contact-form" runat="server"></asp:TextBox>
    <asp:RequiredFieldValidator ID="RequiredFieldValidator2" runat="server" ErrorMessage="**Please Enter Email Address**" ControlToValidate="txtemail"             </asp:RequiredFieldValidator>
    <asp:RegularExpressionValidator ID="RegularExpressionValidator2" runat="server"  Font-Italic="true" ErrorMessage="**Please Enter Valid Email Address**" ControlToValidate="txtemail" ValidationExpression="^([\w-\.]+)@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)|(([\w-]+\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\]?)$"></asp:RegularExpressionValidator> 
</div>

<div>
    <asp:TextBox ID="txtcontact" type="contact" placeholder="Your Contact" runat="server"></asp:TextBox>
    <asp:RequiredFieldValidator ID="RequiredFieldValidator3" runat="server" ErrorMessage="**Please Enter Contact Number" ControlToValidate="txtcontact"></asp:RequiredFieldValidator>
    <asp:RegularExpressionValidator ID="RegularExpressionValidator1" runat="server" ErrorMessage="**Invalid Number**" ControlToValidate="txtcontact" ValidationExpression="[0-9]{10}"></asp:RegularExpressionValidator>
</div>

<div>
    <asp:TextBox ID="txtmessage" placeholder="Your Message" TextMode="MultiLine" class="contact-form" runat="server"></asp:TextBox>
    <asp:RequiredFieldValidator ID="RequiredFieldValidator4" runat="server" ErrorMessage="**Please Enter Your Message**" ControlToValidate="txtmessage"></asp:RequiredFieldValidator>
</div>

<div>
    <asp:Button ID="btnsend" href="#" class="btn btn-transparent white" runat="server" Text="Send Message"  />
    <asp:Label ID="lblsend" runat="server" Text=""></asp:Label>
</div>
 
