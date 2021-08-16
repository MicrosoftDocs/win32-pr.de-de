---
title: Erste Schritte mit Skripterstellung für ADSI
description: Skripterstellung ist nützlich für Systemadministratoren, die Batchskripts für häufig verwendete Aufgaben erstellen möchten.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Erste Schritte mit Skripterstellung für ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a83da0194fb03cdb31430f389dbfbf64327806b1b142be3b9c1c5813696548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839953"
---
# <a name="getting-started-with-scripting-for-adsi"></a>Erste Schritte mit Skripterstellung für ADSI

Skripterstellung ist nützlich für Systemadministratoren, die Batchskripts für häufig verwendete Aufgaben erstellen möchten.

Um mit der Skripterstellung mit ADSI zu beginnen, benötigen Sie einen Computer, auf dem Windows ausgeführt wird oder der bei einer Domäne angemeldet ist, die Daten für Computerkonten im Verzeichnis enthält.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Ein einfaches Skriptbeispiel: Suchen von Namen und Speicherorten von Computerkonten

Erstellen Sie eine neue Textdatei mithilfe eines Text-Editors. Im folgenden Codebeispiel wird veranschaulicht, wie Namen und Speicherorte von Computerkonten gesucht werden.


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



Speichern Sie die Datei als First.vbs. Ändern Sie die Zeile, die mit "objCommand.CommandText" beginnt, um den Pfad zu Ihrer Domäne zu ändern. Geben Sie an der Eingabeaufforderung **cscript First.vbs** für eine Befehlszeile oder First.vbs für Windows Skripterstellung ein. Die Ergebnisse sollten an der Eingabeaufforderung zurückgegeben werden.

Weitere Informationen zur Skripterstellung für ADSI finden Sie unter Skripterstellung für [Active Directory-Dienstschnittstellen.](adsi-scripting-tutorial.md)

 

 




