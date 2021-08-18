---
description: Sie können ein Objekt für WMI in Visual Basic Scripting Edition (VBScript) erstellen, indem Sie eine Verbindung mit WMI herstellen und dann CreateObject aufrufen. In der folgenden Tabelle sind die Methoden in der Skripterstellungs-API für WMI aufgeführt, die die Objekterstellung unterstützen.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Erstellen eines Objekts mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e86dbc649d5feab471485dbdf536cde911c139aeab3b6eb3323b24199438d1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244570"
---
# <a name="creating-an-object-using-vbscript"></a>Erstellen eines Objekts mit VBScript

Sie können ein Objekt für WMI in Visual Basic Scripting Edition (VBScript) erstellen, indem Sie eine Verbindung mit WMI herstellen und [dann CreateObject aufrufen.](/previous-versions//xzysf6hc(v=vs.85)) In der folgenden Tabelle sind die Methoden in der Skripterstellungs-API für WMI aufgeführt, die die Objekterstellung unterstützen.



| Schnittstelle                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting.SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | "WbemScripting.SWbemLocator"       |
| [**SWbemLastError**](swbemlasterror.md)         | "WbemScripting.SWbem.LastError"    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting.SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting.SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting.SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting.SWbemSink"          |



 

Im folgenden Verfahren wird beschrieben, wie Sie ein WMI-Objekt mit VBScript erstellen.

**So erstellen Sie ein WMI-Objekt mit VBScript**

1.  Verbinden mithilfe eines Monikers oder eines [**SWbemLocator-Objekts zu WMI.**](swbemlocator.md)

    Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts.](creating-a-wmi-script.md)

2.  Rufen Sie die VBScript [CreateObject-Methode](/previous-versions//xzysf6hc(v=vs.85)) auf.

    Das folgende Codebeispiel zeigt, wie ein -Objekt erstellt wird.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Wenn Sie in Schritt 1 einen Moniker verwenden, müssen Sie [CreateObject nicht erneut](/previous-versions//xzysf6hc(v=vs.85)) aufrufen.

 

 
