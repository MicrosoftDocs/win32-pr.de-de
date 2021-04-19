---
description: Bietet semisynchrone Zugriffs Funktionen und ein Codebeispiel für die Ausführung eines semisynchronen Methoden Aufrufes.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Erstellen eines semisynchronen Aufrufes mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356298"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>Erstellen eines semisynchronen Aufrufes mit VBScript

Einige WMI-Methoden können große Auflistungen zurückgeben, sodass Skripts nicht mehr reagieren. In Skripts ist der semisynchrone Zugriff der Standard, und in Windows-Verwaltungsinstrumentation (WMI) wird **wbemFlagReturnImmediately** für Aufrufe festgelegt, die große Objekt Auflistungen zurückgeben können, wie z. b. die folgenden [**Swap Services**](swbemservices.md) -Methoden: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**associatorsof**](swbemservices-associatorsof.md)und [**referencesto**](swbemservices-referencesto.md).

Der semisynchrone Zugriff, bei dem **wbemFlagReturnImmediately** im *IFlags* -Parameter festgelegt ist, ist auch die Standardeinstellung für Aufrufe, die große Objekt Sätze für die folgenden " [**errbewbject**](swbemobject.md) "-Methoden zurückgeben können: [**Instanzen \_**](swbemobject-instances-.md), [**Unterklassen \_**](swbemobject-subclasses-.md), [**assoziatoren \_**](swbemobject-associators-.md)und [**Verweise \_**](swbemobject-references-.md).

Um die Verwendung der WMI-Speicher Ressource bei der Verarbeitung einer großen Auflistung von Objekten zu reduzieren, schließen Sie den Wert von **wbemFlagForwardOnly** in den *IFlags* -Parameter ein. Die Verwendung von **wbemFlagForwardOnly** bewirkt, dass WMI einen vorwärts-Enumerator erstellt, der das erneute Auffüllen der Auflistung und das erneute zugreifen auf Elemente nicht zulässt.

WMI entfernt den Arbeitsspeicher für jedes Objekt, da die **for each** -Anweisung ein-Objekt verarbeitet. Die **count** -Methode kann nicht für eine Auflistung aufgerufen werden, wenn das **wbemFlagForwardOnly** -Flag für den-Befehl festgelegt wurde, der die Auflistung abgerufen hat. Beachten Sie, dass für den *IFlags* -Parameter **wbemFlagReturnImmediately** und **wbemFlagForwardOnly** standardmäßig für die [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) -Methode festgelegt ist.

Im folgenden Verfahren wird beschrieben, wie VBScript zum Ausführen eines semisynchronen Aufrufes verwendet wird.

**So führen Sie einen semisynchronen-Befehl in VBScript aus**

1.  Legen Sie den *IFlags* -Parameter auf den Wert von [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)fest.
2.  Führen Sie den normalen synchronen Aufruf für [**SWbemServices.Execquery**](swbemservices-execquery.md) oder [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) mit dem *IFlags* -Wert aus.
3.  Wenn Sie die vom-Befehl zurückgegebenen Objekte als Auflistung behandeln möchten, verwenden Sie **jeweils** eine Enumerationssyntax, z. b. VBScript. Da jedes Objekt zurückgegeben wird, wird es als das nächste Element in der Auflistung verarbeitet.
4.  Erstellen Sie einen vorwärts-Enumerator, indem Sie den Wert von **wbemFlagReturnImmediately** mit dem Wert von **wbemFlagForwardOnly** kombinieren. Der Dezimalwert dieses or-Vorgangs ist 48. Diese Konstanten werden in der wbemdisp. tlb-Typbibliothek für Visual Basic definiert. Die meisten Skriptsprachen verwenden den numerischen Wert oder definieren eine Konstante. Weitere Informationen finden Sie unter [wbemflagenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).

Im folgenden Codebeispiel wird gezeigt, wie Sie einen semisynchronen Methoden aufrufmachen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 



