<template>
    <div class="tab-pane active" id="myprofile" role="tabpanel">
        <div class="row">
            <div class="col-lg-12">
                <div class="col-lg-6">
                    <div class="col-lg-12 tabcontent" id="Information" style="display: block;">
                        <div style="background: #f3f3f3;" class="tab-main-content row col-lg-12 col-md-12 col-sm-12 col-xs-12">
                            <div class="editabl password password-field">
                                <div class="formbox">
                                    <label style="text-align: left" class="col-md-8 col-sm-8 col-xs-8 profupdate">
                                        PERSONAL INFORMATION
                                    </label>

                                    <a class="edit" href="javascript:void(0)" @click="btneditinfo()">
                                        Edit
                                    </a>

                                    <div class="sc_btn">
                                        <a class="save" v-show="!editinfoflag" @click="btnsaveinfo()" >Save</a>
                                        <a class="exit" v-show="!editinfoflag" @click="btnexitinfo()" >Cancel</a>
                                    </div>

                                    <ul class="personal-info">
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-4 col-sm-5 col-xs-12 control-label">
                                                    Gender
                                                </label>
                                                <div style="text-align: left" class="col-md-8 col-sm-7 col-xs-12">
                                                    <div style="float: left" class="form-value">
                                                        <label class="control-label">
                                                            Male
                                                        </label>
                                                    </div>
                                                    <div style="float: left">
                                                        <div style=" margin: 1px 20px;width: 40px;" class="material-switch pull-right">
                                                            <input id="someSwitchOptionDefault" name="someSwitchOption001" type="checkbox">
                                                            <label for="someSwitchOptionDefault" class="label-default">
                                                            </label>
                                                        </div>
                                                    </div>
                                                    <div class="form-value">
                                                        <label class="control-label">
                                                            Female
                                                        </label>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-4 col-sm-5 col-xs-12 control-label">
                                                    Name
                                                </label>
                                                <div style="text-align: left" class="col-md-8 col-sm-7 col-xs-12">
                                                    <div class="form-value">
                                                        <span id="CompanyName">
                                                            Last Name, First Name O.
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-4 col-sm-5 col-xs-12 control-label">
                                                    Birthdate
                                                </label>
                                                <div style="text-align: left" class="col-md-8 col-sm-7 col-xs-12">
                                                    <div class="form-value">
                                                        <span id="CompanyBirthdate">
                                                            Feb. 21, 1993
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-4 col-sm-5 col-xs-12 control-label">
                                                    Location
                                                </label>
                                                <div style="text-align: left" class="col-md-8 col-sm-7 col-xs-12">
                                                    <div class="form-value">
                                                        <span id="CompanyLocation">
                                                            Address st., City, Germany
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-4 col-sm-5 col-xs-12 control-label">
                                                    Contact Number
                                                </label>
                                                <div style="text-align: left" class="col-md-8 col-sm-7 col-xs-12">
                                                    <div class="form-value">
                                                        <span id="CompanyContactNumber">
                                                            +43 9864 7874 986
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="col-lg-12">
                        <div class="col-lg-12 tabcontent" id="Information" style="display: block;">
                            <div style="background: #f3f3f3;" class="tab-main-content row col-lg-12 col-md-12 col-sm-12 col-xs-12">
                                <div class="editabl editable password password-fields formbox">
                                    <label style="text-align: left;" class="col-md-8 col-sm-8 col-xs-8 profupdate">
                                        Email &amp; Password
                                    </label>
                                    <a class="edit" href="javascript:void(0)" @click="btneditaccount()">
                                        Edit
                                    </a>

                                    <div class="sc_btn">
                                        <a class="save" v-show="!editaccountflag" @click="btnsaveaccount()" >Save</a>
                                        <a class="exit" v-show="!editaccountflag" @click="btnexitaccount()" >Cancel</a>
                                    </div>
                                    <ul class="personal-info">
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-6 col-sm-6 col-xs-6 control-label">
                                                    E-mail
                                                </label>
                                                <div style="text-align: left" class="col-md-6 col-sm-6 col-xs-6">
                                                    <div class="form-value">
                                                        <span id="Companyemail">
                                                            email@gmail.com
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-6 col-sm-6 col-xs-6 control-label">
                                                    Password
                                                </label>
                                                <div style="text-align: left" class="col-md-6 col-sm-6 col-xs-6">
                                                    <div class="form-value">
                                                        <span id="CompanyPassword">
                                                            **********
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                        <li>
                                            <div class="form-group">
                                                <label style="text-align: left" class="col-md-6 col-sm-6 col-xs-6 control-label">
                                                    Repeat Password
                                                </label>
                                                <div style="text-align: left" class="col-md-6 col-sm-6 col-xs-6">
                                                    <div class="form-value">
                                                        <span id="CompanyRepeatPassword">
                                                            **********
                                                        </span>
                                                    </div>
                                                </div>
                                            </div>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data:function(){
        return{
            editinfoflag:true,
            editaccountflag:true
        }
    },
    methods:{
        btneditinfo:function(){
            this.editinfoflag=!this.editinfoflag;
            console.log("Edit Info!!!");
        },
        btnsaveinfo:function(){
            this.editinfoflag=!this.editinfoflag;
            console.log("Save Info!!!");
        },
        btnexitinfo:function(){
            this.editinfoflag=!this.editinfoflag;
            console.log("Exit Info!!!");
        },
        btneditaccount:function(){
            this.editaccountflag=!this.editaccountflag;
            console.log("Edit Account!!!");
        },
        btnsaveaccount:function(){
            this.editaccountflag=!this.editaccountflag;
            console.log("Save Account!!!");
        },
        btnexitaccount:function(){
            this.editaccountflag=!this.editaccountflag;
            console.log("Exit Account!!!");
        }
    }
}
</script>
