---
description: Für privilegierte Vorgänge sind Sicherheits Privilegien erforderlich, z. b. SeLoadDriverPrivilege (wbemprivilegeloaddriver in den Scripting API-Konstanten), eine Berechtigung, die für ein Konto aktiviert werden muss, das einen Gerätetreiber lädt.
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
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348916"
---
# <a name="executing-privileged-operations"></a>Ausführen privilegierter Vorgänge

Für privilegierte Vorgänge sind Sicherheits Privilegien erforderlich, z. **b. SeLoadDriverPrivilege** (**wbemprivilegeloaddriver** in den [Scripting API-Konstanten](scripting-api-constants.md)), eine Berechtigung, die für ein Konto aktiviert werden muss, das einen Gerätetreiber lädt. Sie können einem Administrator oder Benutzer über WMI keine Berechtigungen hinzufügen. Sie können nur Berechtigungen aktivieren, die das Konto bereits besitzt. Eine Liste der Berechtigungen finden Sie unter [**Berechtigungs \_ Konstanten**](privilege-constants.md).

Standardmäßig kann ein lokaler Benutzer auf einem Computer statische Daten aus dem [*WMI-Repository*](gloss-w.md)lesen, in Instanzen, die von Anbietern bereitgestellt werden, schreiben und Anbieter Methoden ausführen, es sei denn, der Anbieter erzwingt besondere, eigene Sicherheitsanforderungen. Nur Administratoren können [eine Verbindung mit einem Remote Computer herstellen](connecting-to-wmi-on-a-remote-computer.md), Sicherheits Deskriptoren ändern oder statische WMI-Repository-Daten wie z. b. eine WMI-Klassendefinition ändern. Alle Berechtigungen sind für eine Remote Verbindung aktiviert. Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).

Die Berechtigungs Konstanten für C++ unterscheiden sich von denen, die von Automatisierungs Sprachen wie z. b. Visual Basic verwendet werden. Skripts müssen den Wert der Konstante anstelle des Namens verwenden. Weitere Informationen finden Sie unter [Ausführen von privilegierten Vorgängen mithilfe von C++](executing-privileged-operations-using-c-.md) oder [Ausführen privilegierter Vorgänge mithilfe von VBScript](executing-privileged-operations-using-vbscript.md).

Eine häufige Ursache für Zugriffs Verweigerungs Fehler bei der Verwendung von WMI ist das Fehlen einer aktivierten Berechtigung für Vorgänge, z. b. das Abrufen aller Instanzen von [**Win32 \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Wenn Sie die **sesecurity** -Berechtigung nicht aktivieren, können Sie nicht auf die Sicherheitsprotokoll Datei zugreifen.

Im folgenden VBScript-Codebeispiel wird gezeigt, wie die **sesecurity** -Berechtigung in der Monikerzeichenfolge festgelegt wird. Bei Verwendung im Moniker löscht der Berechtigungs Name in Klammern den ursprünglichen "SE". Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md).


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

[**Berechtigungs Konstanten**](privilege-constants.md)
</dt> </dl>

 

 
