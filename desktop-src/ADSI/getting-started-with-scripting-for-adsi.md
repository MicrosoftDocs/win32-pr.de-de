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
# <a name="getting-started-with-scripting-for-adsi"></a>Einstieg in die Skripterstellung für ADSI

Die Skripterstellung ist hilfreich für Systemadministratoren, die Batch Skripts für häufig verwendete Aufgaben erstellen möchten.

Um mit der Skripterstellung mit ADSI zu beginnen, müssen Sie über einen Computer verfügen, auf dem Windows ausgeführt wird oder der bei einer Domäne angemeldet ist, die Daten für Computer Konten im Verzeichnis enthält.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Ein einfaches Beispiel für die Skripterstellung: Suchen nach Namen und Speicherorten von Computer Konten

Erstellen Sie eine neue Textdatei mit einem Text-Editor. Im folgenden Codebeispiel wird gezeigt, wie Namen und Speicherorte von Computer Konten gefunden werden.


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



Speichern Sie die Datei als First.vbs. Ändern Sie die Zeile, die mit "objCommand. CommandText" beginnt, um den Pfad zu Ihrer Domäne zu ändern. Geben Sie an der Eingabeaufforderung **cscript-First.vbs** für eine Befehlszeile oder First.vbs für die Windows-Skripterstellung ein. Die Ergebnisse sollten an der Eingabeaufforderung zurückgegeben werden.

Weitere Informationen zur Skripterstellung für ADSI finden Sie unter [Active Directory-Dienst Schnittstellen Skript](adsi-scripting-tutorial.md)Erstellung.

 

 




