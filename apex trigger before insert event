trigger EmpInsert on Employee__c (before insert) {

	for(Employee__c pass : Trigger.New){

	List<Employee__c> mynew = [SELECT Id, Name FROM Employee__c WHERE Employee_Name__c =: pass.Employee_Name__c];

		if(mynew.size() > 0){

        	pass.Name.addError('Employee with same name is existing');

     	} 

    }
}
