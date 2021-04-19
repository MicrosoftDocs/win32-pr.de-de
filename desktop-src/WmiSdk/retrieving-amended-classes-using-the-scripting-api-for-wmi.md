---
description: Wenn Sie die Skript-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema als Teil eines Monikers an.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Abrufen von geänderten Klassen mithilfe der Skript-API für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348889"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Abrufen von geänderten Klassen mithilfe der Skript-API für WMI

Wenn Sie die Skript-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema als Teil eines Monikers an. Oder Sie können den Gebiets Schema Namen im "" "" "" " *" der Methode* "" von "" "" [**".**](swbemlocator-connectserver.md) Wenn Sie geänderte Klassen lesen oder schreiben möchten, geben Sie an, dass Sie lokalisierte Klassendefinitionen verwenden möchten, indem Sie [wbemflaguseamendedqualifizierer](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) als Flag für den *IFlags* -Parameter der aufzurufenden Methode angeben. Für PowerShell können Sie den *-locale-* Parameter für [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) verwenden, um das Gebiets Schema anzugeben.

Im folgenden Codebeispiel wird gezeigt, wie eine lokalisierte Klasse mit einem WMI-skriptingmoniker oder dem-locale-Parameter abgerufen wird.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





Im folgenden Codebeispiel wird gezeigt, wie Sie den locale-Parameter festlegen und das [wbemflaguseamendedqualifizierungsflag](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) verwenden.


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

In der folgenden Tabelle werden die Methoden aufgelistet, die das [wbemflaguseamendedqualifizierungsflag](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) akzeptieren.



| Synchrone Methode                                                 | Asynchrone Methode                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Swap Services. SubclassesOf**](swbemservices-subclassesof.md)   | [**Austausch Services. subclassesofasync**](swbemservices-subclassesofasync.md)   |
| [**Swap. subclasses\_**](swbemobject-subclasses-.md)        | [**Austauschen von "errbemubject. subclassesasync"\_**](swbemobject-subclassesasync-.md)        |
| [**Swap Services. InstancesOf**](swbemservices-instancesof.md)     | [**Swap Services. instancesofasync**](swbemservices-instancesofasync.md)     |
| [**"Errbemubject. Instance"\_**](swbemobject-instances-.md)          | [**Austauschen von "errbemubject. instancesasync"\_**](swbemobject-instancesasync-.md)          |
| [**CquerySWbemServices.Exe**](swbemservices-execquery.md)         | [**CqueryasyncSWbemServices.Exe**](swbemservices-execqueryasync.md)         |
| [**Austauschdienste. Get**](swbemservices-get.md)                     | [**"Swap Services. getasync"**](swbemservices-getasync.md)                     |
| [**Swap-Datei\_**](swbemobject-put-.md)                      | [**Austauschen von "errbemubject. putasync"\_**](swbemobject-putasync-.md)                      |
| [**"Swap Services. referencesto"**](swbemservices-referencesto.md)   | [**"Swap Services. referencestoasync"**](swbemservices-referencestoasync.md)   |
| [**"Errbemubject. References"\_**](swbemobject-references-.md)        | [**Austauschen von "errbemubject. referencesasync"\_**](swbemobject-referencesasync-.md)        |
| [**"Taubemservices. associatorsof"**](swbemservices-associatorsof.md) | [**Swap Services. associatorsofasync**](swbemservices-associatorsofasync.md) |
| [**"Errbemujeject. ASSOCIATORS"\_**](swbemobject-associators-.md)      | [**"Errbemubject. associatorsasync"\_**](swbemobject-associatorsasync-.md)      |



 

 

 
