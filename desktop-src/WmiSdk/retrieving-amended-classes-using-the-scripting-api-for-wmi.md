---
description: Wenn Sie die Skripterstellungs-API für WMI verwenden, um lokalisierte Klasseninformationen abzurufen oder zu speichern, geben Sie das Gebietsschema als Teil eines Monikers an.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Abrufen von geänderten Klassen mithilfe der Skripterstellungs-API für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47d01af2515b26ca308a1b258aa40508f227a0c1d0eaa5b2b332c1e7b3200420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130882"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Abrufen von geänderten Klassen mithilfe der Skripterstellungs-API für WMI

Wenn Sie die Skripterstellungs-API für WMI verwenden, um lokalisierte Klasseninformationen abzurufen oder zu speichern, geben Sie das Gebietsschema als Teil eines Monikers an. Alternativ können Sie den Gebietsschemanamen im *strLocale-Parameter* für die [**SWbemLocator.ConnectServer-Methode**](swbemlocator-connectserver.md) angeben. Geben Sie beim Lesen oder Schreiben geänderter Klassen an, dass Sie lokalisierte Klassendefinitionen verwenden möchten, indem Sie [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) als Flag für den *iFlags-Parameter* der aufgerufenen Methode angeben. Für PowerShell können Sie den Parameter *-locale* in [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) verwenden, um das Gebietsschema anzugeben.

Das folgende Codebeispiel zeigt, wie eine lokalisierte Klasse mithilfe eines WMI-Skriptmonikers oder des Parameters -locale abgerufen wird.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





Das folgende Codebeispiel zeigt, wie sie den Gebietsschemaparameter festlegen und das [Flag wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) verwenden.


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der gleichen Authentifizierungsebene zurückgegeben wird, die der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchron zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

In der folgenden Tabelle sind die Methoden aufgeführt, die das [Flag wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) akzeptieren.



| Synchrone Methode                                                 | Asynchrone Methode                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)   | [**SWbemServices.SubclassesOfAsync**](swbemservices-subclassesofasync.md)   |
| [**SWbemObject.Subclasses\_**](swbemobject-subclasses-.md)        | [**SWbemObject.SubclassesAsync\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)     | [**SWbemServices.InstancesOfAsync**](swbemservices-instancesofasync.md)     |
| [**SWbemObject.Instances\_**](swbemobject-instances-.md)          | [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExecQuery**](swbemservices-execquery.md)         | [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)         |
| [**SWbemServices.Get**](swbemservices-get.md)                     | [**SWbemServices.GetAsync**](swbemservices-getasync.md)                     |
| [**SWbemObject.Put\_**](swbemobject-put-.md)                      | [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)   | [**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)   |
| [**SWbemObject.References\_**](swbemobject-references-.md)        | [**SWbemObject.ReferencesAsync\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md) | [**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md) |
| [**SWbemObject.Associators\_**](swbemobject-associators-.md)      | [**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)      |



 

 

 
