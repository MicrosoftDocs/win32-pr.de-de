---
description: Sie können die Eigenschaften des Objekts "Swap Method" verwenden, um eine einzelne Methoden Definition eines WMI-Objekts zu überprüfen. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Taubemmethod-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528487"
---
# <a name="swbemmethod-object"></a>Taubemmethod-Objekt

Sie können die Eigenschaften des Objekts " **Swap Method** " verwenden, um eine einzelne Methoden Definition eines WMI-Objekts zu überprüfen. Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.

Dieses Objekt kann verwendet werden, um die Definitionen von-Methoden zu überprüfen. Um die Methoden aufzurufen, sollten Sie entweder den direkten Zugriff (siehe Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md)) für ein " [**errbemubject**](swbemobject.md) " (das empfohlene Mechanismus) oder den [**SWbemServices.Execmethod**](swbemservices-execmethod.md) -Aufruf verwenden.

> [!Note]  
> In dieser Version der API wird Schreibzugriff auf Methoden Informationen nicht unterstützt. Wenn Sie Methoden definieren oder vorhandene Methoden Definitionen ändern möchten, können Sie die Methoden Änderungen in einer MOF-Datei definieren und die Änderungen mithilfe des [MOF-Compilers](compiling-mof-files.md)übermitteln. Verwenden Sie alternativ die [com-API für WMI](com-api-for-wmi.md).

 

## <a name="members"></a>Member

Das Objekt " **Swap-Methode** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das Objekt " **Swap-Methode** " verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**InParameters**](swbemmethod-inparameters.md)<br/>   | Schreibgeschützt<br/> | Ein [**-**](swbemobject.md) Objekt, dessen Eigenschaften die Eingabeparameter für diese Methode definieren.<br/>              |
| [**Name**](swbemmethod-name.md)<br/>                   | Schreibgeschützt<br/> | Der Name der Methode.<br/>                                                                                                     |
| [**Entstehungs**](swbemmethod-origin.md)<br/>               | Schreibgeschützt<br/> | Die Ursprungs Klasse der Methode.<br/>                                                                                        |
| [**OutParameters**](swbemmethod-outparameters.md)<br/> | Schreibgeschützt<br/> | Ein [**-**](swbemobject.md) Objekt, dessen Eigenschaften die Out-Parameter und den Rückgabetyp dieser Methode definieren.<br/> |
| [**Qualifikation\_**](swbemmethod-qualifiers-.md)<br/>    | Schreibgeschützt<br/> | Ein [**-**](swbemqualifierset.md) Objekt, das die Qualifizierer für diese Methode enthält.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Methode<br/>                                                           |
| IID<br/>                      | IID \_ iswbemmethod<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




