---
description: Dieser Beispielcode basiert auf einer benutzerdefinierten Ice-Aktion (ICE08). Das Eis überprüft, ob jede Komponente in der Komponenten Tabelle über eine eindeutige GUID verfügt. Wenn die Komponenten Tabelle nicht vorhanden ist, wird keine Validierung durchgeführt.
ms.assetid: 785c3fd6-7120-4532-b055-b73a9a44f75d
title: Sample Ice in VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf49c37eb5aa8d8e4b4e7b617802c49389e77ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350235"
---
# <a name="sample-ice-in-vbscript"></a><span data-ttu-id="60952-105">Sample Ice in VBScript</span><span class="sxs-lookup"><span data-stu-id="60952-105">Sample ICE in VBScript</span></span>

<span data-ttu-id="60952-106">Dieser Beispielcode basiert auf einer benutzerdefinierten Ice-Aktion ( [ICE08](ice08.md)).</span><span class="sxs-lookup"><span data-stu-id="60952-106">This sample code is from an ICE custom action ( [ICE08](ice08.md)).</span></span> <span data-ttu-id="60952-107">Das Eis überprüft, ob jede Komponente in der [Komponenten Tabelle](component-table.md) über eine eindeutige [GUID](guid.md)verfügt.</span><span class="sxs-lookup"><span data-stu-id="60952-107">The ICE validates that every component in the [Component table](component-table.md) has a unique [GUID](guid.md).</span></span> <span data-ttu-id="60952-108">Wenn die Komponenten Tabelle nicht vorhanden ist, wird keine Validierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="60952-108">No validation is done if the Component table does not exist.</span></span>


```VB
Function ICE08()

'Give creation data
Set recInfo=Installer.CreateRecord(1)
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Created 05/21/98 by <insert 
    author's name here>"
Message &h03000000, recInfo

'Give last modification date
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Modified 05/21/98 by <insert 
    author's name here>"
Message &h03000000, recInfo

'Give description of test
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Checks for duplicate GUIDs 
    in Component table"
Message &h03000000, recInfo

'Is there a Component table in the database?
iStat = Database.TablePersistent("Component")
If 1 <> iStat Then
recInfo.StringData(0)="ICE08" & Chr(9) & "2" 
    & Chr(9) & "Table: 'Component' missing. 
    ICE08 cannot continue its validation." 
    & Chr(9) & "https://mypage2"
Message &h03000000, recInfo
ICE08 = 1
Exit Function
End If

'process component table
Set view=Database.OpenView("SELECT 
    `Component`,`ComponentId` FROM 
    `Component` ORDER BY `ComponentId`")
view.Execute
Do
Set rec=view.Fetch
If rec Is Nothing Then Exit Do

'compare for duplicate 
If lastGuid=rec.StringData(2) Then
rec.StringData(0)="ICE08" & Chr(9) 
    & "1" & Chr(9) & "Component: [1] 
    has a duplicate GUID: [2]" & Chr(9) 
    & "https://mypage2" & Chr(9) & 
    "Component" & Chr(9) & "ComponentId" & Chr(9) & "[1]"
Message &h03000000,rec
End If

'set for next compare
lastGuid=rec.StringData(2)
Loop

'Return iesSuccess 
ICE08 = 1

End Function
```



 

 



