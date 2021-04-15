---
description: Im Autorisierungs-Manager ist ein Vorgang eine Funktion oder Methode einer Anwendung auf niedriger Ebene.
ms.assetid: 6b35d25e-150c-4760-b358-fa517a00dd79
title: Definieren von Vorgängen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ef1337bc8e5c44ccce25e3f6d87f7cf6240d2d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350578"
---
# <a name="defining-operations-in-script"></a>Definieren von Vorgängen in Skripts

Im Autorisierungs-Manager ist ein Vorgang eine Funktion oder Methode einer Anwendung auf niedriger Ebene. Diese Vorgänge werden als Aufgaben zusammengefasst. Benutzer der Anwendung fordern die Berechtigung zum Ausführen von Aufgaben an. Ein Vorgang wird durch ein [**iazoperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) -Objekt dargestellt. Weitere Informationen zu Vorgängen finden Sie unter [Vorgänge und Aufgaben](operations-and-tasks.md).

Im folgenden Beispiel wird gezeigt, wie Vorgänge in einem Autorisierungs Richtlinien Speicher definiert werden. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist und dass dieser Speicher eine Anwendung mit dem Namen "Aufwendungen" enthält.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create operations.

'  Create first operation.
Dim Op1
Set Op1 = expenseApp.CreateOperation("RetrieveForm")

'  Set the OperationID property.
Op1.OperationID = 1

'  Save the operation to the store.
Op1.Submit

'  Create second operation.
Dim Op2
Set Op2 = expenseApp.CreateOperation("EnqueRequest")

'  Set the OperationID property.
Op2.OperationID = 2

'  Save the operation to the store.
Op2.Submit

'  Create third operation.
Dim Op3
Set Op3 = expenseApp.CreateOperation("DequeRequest")

'  Set the OperationID property.
Op3.OperationID = 3

'  Save the operation to the store.
Op3.Submit

'  Create fourth operation.
Dim Op4
Set Op4 = expenseApp.CreateOperation("UseFormControl")

'  Set the OperationID property.
Op4.OperationID = 4

'  Save the operation to the store.
Op4.Submit

'  Create fifth operation.
Dim Op5
Set Op5 = expenseApp.CreateOperation("MarkFormApproved")

'  Set the OperationID property.
Op5.OperationID = 5

'  Save the operation to the store.
Op5.Submit

'  Create sixth operation.
Dim Op6
Set Op6 = expenseApp.CreateOperation("SendApprovalNotify")

'  Set the OperationID property.
Op6.OperationID = 6

'  Save the operation to the store.
Op6.Submit
```



 

 



