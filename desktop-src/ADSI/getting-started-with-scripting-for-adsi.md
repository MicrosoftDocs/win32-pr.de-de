---
title: Einstieg in die Skripterstellung für ADSI
description: Die Skripterstellung ist hilfreich für Systemadministratoren, die Batch Skripts für häufig verwendete Aufgaben erstellen möchten.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Einstieg in die Skripterstellung für ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947341"
---
# <a name="getting-started-with-scripting-for-adsi"></a><span data-ttu-id="5fbd0-104">Einstieg in die Skripterstellung für ADSI</span><span class="sxs-lookup"><span data-stu-id="5fbd0-104">Getting Started with Scripting for ADSI</span></span>

<span data-ttu-id="5fbd0-105">Die Skripterstellung ist hilfreich für Systemadministratoren, die Batch Skripts für häufig verwendete Aufgaben erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-105">Scripting is useful for system administrators who want to create batch scripts for frequently used tasks.</span></span>

<span data-ttu-id="5fbd0-106">Um mit der Skripterstellung mit ADSI zu beginnen, müssen Sie über einen Computer verfügen, auf dem Windows ausgeführt wird oder der bei einer Domäne angemeldet ist, die Daten für Computer Konten im Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-106">To start scripting with ADSI, you must have a computer that runs Windows or be logged on to a domain that contains data for computer accounts in the directory.</span></span>

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a><span data-ttu-id="5fbd0-107">Ein einfaches Beispiel für die Skripterstellung: Suchen nach Namen und Speicherorten von Computer Konten</span><span class="sxs-lookup"><span data-stu-id="5fbd0-107">A Simple Scripting Sample: Finding Names and Locations of Computer Accounts</span></span>

<span data-ttu-id="5fbd0-108">Erstellen Sie eine neue Textdatei mit einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-108">Create a new text file using a text editor.</span></span> <span data-ttu-id="5fbd0-109">Im folgenden Codebeispiel wird gezeigt, wie Namen und Speicherorte von Computer Konten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-109">The following code example shows how to find names and locations of computer accounts.</span></span>


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



<span data-ttu-id="5fbd0-110">Speichern Sie die Datei als First.vbs.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-110">Save the file as First.vbs.</span></span> <span data-ttu-id="5fbd0-111">Ändern Sie die Zeile, die mit "objCommand. CommandText" beginnt, um den Pfad zu Ihrer Domäne zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-111">Modify the line that begins with "objCommand.CommandText" to change the path to your domain.</span></span> <span data-ttu-id="5fbd0-112">Geben Sie an der Eingabeaufforderung **cscript-First.vbs** für eine Befehlszeile oder First.vbs für die Windows-Skripterstellung ein.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-112">At the command prompt, type **cscript First.vbs** for a command line or First.vbs for Windows scripting.</span></span> <span data-ttu-id="5fbd0-113">Die Ergebnisse sollten an der Eingabeaufforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-113">The results should be returned in the command prompt.</span></span>

<span data-ttu-id="5fbd0-114">Weitere Informationen zur Skripterstellung für ADSI finden Sie unter [Active Directory-Dienst Schnittstellen Skript](adsi-scripting-tutorial.md)Erstellung.</span><span class="sxs-lookup"><span data-stu-id="5fbd0-114">For more information about scripting for ADSI, see [Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).</span></span>

 

 




