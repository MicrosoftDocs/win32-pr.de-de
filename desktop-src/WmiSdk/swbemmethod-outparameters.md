---
description: Die OutParameters-Eigenschaft des SWbemMethod-Objekts ist ein SWbemObject-Objekt, dessen Eigenschaften die out-Parameter und den Rückgabetyp dieser Methode definieren. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: SWbemMethod.OutParameters-Eigenschaft (Wbemdisp.h)
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
ms.openlocfilehash: 5dec1b2fe18dae65443b45ee6c1d2efcd1d924a72eb2817869c35406ebbc7808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314412"
---
# <a name="swbemmethodoutparameters-property"></a>SWbemMethod.OutParameters (Eigenschaft)

Die **OutParameters-Eigenschaft** des [**SWbemMethod-Objekts**](swbemmethod.md) ist ein [**SWbemObject-Objekt,**](swbemobject.md) dessen Eigenschaften die out-Parameter und den Rückgabetyp dieser Methode definieren. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Weitere Informationen zur Verwendung dieser Eigenschaft zum Abrufen von Ausgabeparametern von Anbietermethoden finden Sie unter [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Beachten Sie, dass alle an diesem Objekt vorgenommenen Änderungen nicht in der zugrunde liegenden Methodendefinition widergespiegelt werden.

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

[**SWbemMethod**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




