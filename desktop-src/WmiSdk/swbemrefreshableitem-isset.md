---
description: Die SWbemRefreshableItem.IsSet-Eigenschaft ist ein boolescher Wert, der angibt, ob das SWbemRefreshableItem-Objekt ein einzelnes Objekt oder einen Objektsatz darstellt. Das SWbemRefreshableItem-Objekt stellt ein einzelnes Objekt oder einen Objektsatz dar.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: SWbemRefreshableItem.IsSet-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312919"
---
# <a name="swbemrefreshableitemisset-property"></a>SWbemRefreshableItem.IsSet (Eigenschaft)

Die **SWbemRefreshableItem.IsSet-Eigenschaft** ist ein boolescher Wert, der angibt, ob das [**SWbemRefreshableItem-Objekt**](swbemrefreshableitem.md) ein einzelnes Objekt oder einen Objektsatz darstellt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Wenn **SWbemRefreshableItem.IsSet** **true** ist, stellt das Element ein [**SWbemObjectSet-Objekt**](swbemobjectset.md) dar, und die [**Object-Eigenschaft**](swbemrefreshableitem-object.md) ist **NULL.** False **gibt an,** dass das Element ein [**SWbemObject-Objekt**](swbemobject.md) darstellt und die **Object-Eigenschaft** **NULL ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




