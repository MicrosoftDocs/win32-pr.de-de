---
description: Sie können ein Objekt für WMI in Visual Basic Scripting Edition (VBScript) erstellen, indem Sie eine Verbindung mit WMI herstellen und dann CreateObject aufrufen. In der folgenden Tabelle sind die Methoden in der Skript-API für WMI aufgelistet, die die Objekt Erstellung unterstützen.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Erstellen eines Objekts mithilfe von VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485355"
---
# <a name="creating-an-object-using-vbscript"></a>Erstellen eines Objekts mithilfe von VBScript

Sie können ein Objekt für WMI in Visual Basic Scripting Edition (VBScript) erstellen, indem Sie eine Verbindung mit WMI herstellen und dann [CreateObject](/previous-versions//xzysf6hc(v=vs.85))aufrufen. In der folgenden Tabelle sind die Methoden in der Skript-API für WMI aufgelistet, die die Objekt Erstellung unterstützen.



| Schnittstelle                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**Swap-DateTime**](swbemdatetime.md)           | "WbemScripting. Swap Time"      |
| [**SWbemLocator**](swbemlocator.md)             | "WbemScripting. Swap-Locator"       |
| [**Austausch Fehler**](swbemlasterror.md)         | "WbemScripting. taubem. LastError"    |
| [**Errbemubjectpath**](swbemobjectpath.md)       | "WbemScripting. errbewbjectpath"    |
| [**Austausch Elementname**](swbemnamedvalueset.md) | "WbemScripting. Swap Name Name" |
| [**Swap-Aktualisierungs Programm**](swbemrefresher.md)         | "WbemScripting. Swap-Aktualisierungs Programm"     |
| [**Swap-Senke**](swbemsink.md)                   | "WbemScripting. taubemsink"          |



 

Im folgenden Verfahren wird beschrieben, wie ein WMI-Objekt mit VBScript erstellt wird.

**So erstellen Sie ein WMI-Objekt mithilfe von VBScript**

1.  Stellen Sie eine Verbindung mit WMI her, indem Sie entweder einen Moniker oder ein [**Swap**](swbemlocator.md) -Objekt verwenden.

    Weitere Informationen finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).

2.  Aufrufen der VBScript-Methode "| [ateobject](/previous-versions//xzysf6hc(v=vs.85)) ".

    Im folgenden Codebeispiel wird gezeigt, wie ein-Objekt erstellt wird.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Wenn Sie in Schritt 1 einen Moniker verwenden, müssen Sie " [kreateobject](/previous-versions//xzysf6hc(v=vs.85)) " nicht erneut aufrufen.

 

 
