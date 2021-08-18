---
description: Sie können die Eigenschaften des SWbemMethod-Objekts verwenden, um eine einzelne Methodendefinition eines WMI-Objekts zu überprüfen. Dieses Objekt kann nicht durch den VBScript-CreateObject-Aufruf erstellt werden.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: SWbemMethod-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c750e81a3e41450e8cd32f37ccab6fee2f08439c6bc8fc8ae18bf0e4f106b551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732660"
---
# <a name="swbemmethod-object"></a>SWbemMethod-Objekt

Sie können die Eigenschaften des **SWbemMethod-Objekts** verwenden, um eine einzelne Methodendefinition eines WMI-Objekts zu überprüfen. Dieses Objekt kann nicht durch den **VBScript-CreateObject-Aufruf** erstellt werden.

Dieses Objekt kann verwendet werden, um die Definitionen von Methoden zu überprüfen. Um die Methoden aufzurufen, sollten Sie entweder direkten Zugriff (siehe [Bearbeiten von Klassen- und Instanzinformationen)](manipulating-class-and-instance-information.md)für ein [**SWbemObject-Objekt**](swbemobject.md) (der empfohlene Mechanismus) oder den [**SWbemServices.ExecMethod-Aufruf**](swbemservices-execmethod.md) verwenden.

> [!Note]  
> In dieser Version der API wird der Schreibzugriff auf Methodeninformationen nicht unterstützt. Wenn Sie Methoden definieren oder vorhandene Methodendefinitionen ändern möchten, können Sie die Methodenänderungen in einer MOF-Datei definieren und die Änderungen mit dem [MOF-Compiler](compiling-mof-files.md)übermitteln. Alternativ können Sie die [COM-API für WMI](com-api-for-wmi.md)verwenden.

 

## <a name="members"></a>Member

Das **SWbemMethod-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **SWbemMethod-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | Beschreibung                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**InParameters**](swbemmethod-inparameters.md)<br/>   | Schreibgeschützt<br/> | Ein [**SWbemObject-Objekt,**](swbemobject.md) dessen Eigenschaften die Eingabeparameter für diese Methode definieren.<br/>              |
| [**Name**](swbemmethod-name.md)<br/>                   | Schreibgeschützt<br/> | Der Name der Methode.<br/>                                                                                                     |
| [**Origin**](swbemmethod-origin.md)<br/>               | Schreibgeschützt<br/> | Ursprungsklasse der -Methode.<br/>                                                                                        |
| [**OutParameters**](swbemmethod-outparameters.md)<br/> | Schreibgeschützt<br/> | Ein [**SWbemObject-Objekt,**](swbemobject.md) dessen Eigenschaften die out-Parameter und den Rückgabetyp dieser Methode definieren.<br/> |
| [**Qualifikation\_**](swbemmethod-qualifiers-.md)<br/>    | Schreibgeschützt<br/> | Ein [**SWbemQualifierSet-Objekt,**](swbemqualifierset.md) das die Qualifizierer für diese Methode enthält.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




