# ASP.NET-Contact-Page-Validations
Textbox, Contact Number, Email Address, Submit Button Validations Included. 

 <form runat="server">

                                            <asp:TextBox ID="txtname" type="text" placeholder="Your Name" class="contact-form" runat="server"></asp:TextBox>
                                            <asp:RequiredFieldValidator ID="RequiredFieldValidator1" runat="server" ErrorMessage="**Please Enter Your Name**"                                                                   ControlToValidate="txtname"></asp:RequiredFieldValidator>
                                           
                                            <asp:TextBox ID="txtemail" type="email" placeholder="Your Email" class="contact-form" runat="server"></asp:TextBox>
                                            <asp:RequiredFieldValidator ID="RequiredFieldValidator2" runat="server" ErrorMessage="**Please Enter Email Address**"                                                               ControlToValidate="txtemail"></asp:RequiredFieldValidator>
                                            <asp:RegularExpressionValidator ID="RegularExpressionValidator2" runat="server"  Font-Italic="true" ErrorMessage="**Please Enter Valid                                             Email Address**" ControlToValidate="txtemail" ValidationExpression="^([\w-\.]+)@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)|                                                          (([\w-]+\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\]?)$"></asp:RegularExpressionValidator>  

                                            <asp:TextBox ID="txtmessage" placeholder="Your Message" TextMode="MultiLine" class="contact-form" runat="server"></asp:TextBox>
                                            <asp:RequiredFieldValidator ID="RequiredFieldValidator3" runat="server" ErrorMessage="**Please Enter Your Message**"                                                               ControlToValidate="txtmessage"></asp:RequiredFieldValidator>
                                           
                                            <center><div><asp:Button ID="btnsend" href="#" class="btn btn-transparent white" runat="server" Text="Send Message"                                                                 OnClick="btnsend_Click" />
                                            <asp:Label ID="lblsend" runat="server" Text=""></asp:Label> </div> 
                                            </center>
                                        </form>
 
