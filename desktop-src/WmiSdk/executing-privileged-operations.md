---
description: Privilegierte Vorgänge erfordern Sicherheitsberechtigungen wie SeLoadDriverPrivilege (wbemPrivilegeLoadDriver in den Skripterstellungs-API-Konstanten), eine Berechtigung, die für ein Konto aktiviert werden muss, das einen Gerätetreiber lädt.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce87a5783462be86d6e2e2b0565e93d811b972393319a34f84be2ab3d8e34c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050868"
---
# <a name="executing-privileged-operations"></a>Ausführen privilegierter Vorgänge

Privilegierte Vorgänge erfordern Sicherheitsberechtigungen wie **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in den [Skripterstellungs-API-Konstanten](scripting-api-constants.md)), eine Berechtigung, die für ein Konto aktiviert werden muss, das einen Gerätetreiber lädt. Sie können einem Administrator oder Benutzer über WMI keine Berechtigungen hinzufügen. Sie können nur Berechtigungen aktivieren, über die das Konto bereits verfügt. Eine Liste der Berechtigungen finden Sie unter [**Privilege \_ Constants**](privilege-constants.md).

Standardmäßig kann ein lokaler Benutzer auf einem Computer statische Daten aus dem [*WMI-Repository*](gloss-w.md)lesen, in von Anbietern bereitgestellte Instanzen schreiben und Anbietermethoden ausführen, es sei denn, der Anbieter erzwingt eigene spezielle Sicherheitsanforderungen. Nur Administratoren können [eine Verbindung mit einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)herstellen, Sicherheitsbeschreibungen ändern oder statische WMI-Repositorydaten ändern, z. B. eine WMI-Klassendefinition. Alle Berechtigungen sind für eine Remoteverbindung aktiviert. Weitere Informationen finden Sie unter [Sichern einer WMI-Remoteverbindung.](securing-a-remote-wmi-connection.md)

Die Berechtigungskonst constants für C++ unterscheiden sich von denen, die von Automatisierungssprachen wie Visual Basic. Skripts müssen den Wert der Konstante anstelle des Namens verwenden. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge mit C++](executing-privileged-operations-using-c-.md) oder [Ausführen privilegierter Vorgänge mit VBScript.](executing-privileged-operations-using-vbscript.md)

Eine häufige Ursache für Fehler beim Verweigerten Zugriff bei der Verwendung von WMI ist das Fehlen einer aktivierten Berechtigung für Vorgänge, z. B. das Abrufen aller Instanzen von [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Ohne aktivierung der **SeSecurity-Berechtigung** können Sie nicht auf die Sicherheitsprotokolldatei zugreifen.

Das folgende VBScript-Codebeispiel zeigt, wie die **SeSecurity-Berechtigung** in der Monikerzeichenfolge festgelegt wird. Bei Verwendung im Moniker löscht der Berechtigungsname in Klammern das anfängliche "Se". Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge.](constructing-a-moniker-string.md)


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Berechtigungskonst constants**](privilege-constants.md)
</dt> </dl>

 

 
