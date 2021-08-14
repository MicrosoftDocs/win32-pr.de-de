---
title: IWMPMedia2-Fehlereigenschaft
description: Die Error-Eigenschaft ruft eine IWMPErrorItem-Schnittstelle ab, wenn das Medienelement eine Fehlerbedingung aufweist.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Fehlereigenschaft Windows Media Player
- Fehlereigenschaft Windows Media Player , IWMPMedia2-Schnittstelle
- IWMPMedia2-Schnittstelle Windows Media Player , Error-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c841e52f2a5adda5a2098f591b141aa334ee5138c1a5cc7d6eff9b54dca5e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331970"
---
# <a name="iwmpmedia2error-property"></a>IWMPMedia2::Error-Eigenschaft

Die **Error-Eigenschaft** ruft eine **IWMPErrorItem-Schnittstelle** ab, wenn das Medienelement eine Fehlerbedingung aufweist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib.IWMPErrorItem-Schnittstelle,** die Zugriff auf Informationen zur Fehlerbedingung bietet.

## <a name="remarks"></a>Hinweise

Wenn das Medienelement nicht wiedergegeben werden kann, ruft diese Eigenschaft eine **IWMPErrorItem-Schnittstelle** ab, die Informationen zum aufgetretenen Problem enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPErrorItem (VB und C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPMedia2-Schnittstelle (VB und C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





