---
description: Die OutParameters-Eigenschaft des "errbemmethod"-Objekts ist ein Objekt vom Typ "OutParameters", dessen Eigenschaften die Out-Parameter und den Rückgabetyp dieser Methode definieren. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: "' Taubemmethod. OutParameters '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353547"
---
# <a name="swbemmethodoutparameters-property"></a>' Taubemmethod. OutParameters '-Eigenschaft

Die **OutParameters** -Eigenschaft des " [**errbemmethod**](swbemmethod.md) "- [**Objekts ist ein Objekt**](swbemobject.md) vom Typ "OutParameters", dessen Eigenschaften die Out-Parameter und den Rückgabetyp dieser Methode definieren. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zur Verwendung dieser Eigenschaft zum Abrufen von Ausgabeparametern von Anbieter Methoden finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Beachten Sie, dass alle an diesem Objekt vorgenommenen Änderungen nicht in der zugrunde liegenden Methoden Definition widergespiegelt werden.

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

[**Swap-Methode**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.Execmethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.Execmethodasync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.Execmethod**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




