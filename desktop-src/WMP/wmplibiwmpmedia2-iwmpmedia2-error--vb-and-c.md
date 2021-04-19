---
title: IWMPMedia2 Error (Eigenschaft)
description: Die Error-Eigenschaft ruft eine iwmperroritem-Schnittstelle ab, wenn das Medien Element einen Fehlerzustand aufweist.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Fehler Eigenschaften Fenster Media Player
- Fehler Eigenschaft, Windows Media Player, IWMPMedia2-Schnittstelle
- IWMPMedia2 Interface, Windows Media Player, Fehler Eigenschaft
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
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355266"
---
# <a name="iwmpmedia2error-property"></a>IWMPMedia2:: Error (Eigenschaft)

Die **Error** -Eigenschaft ruft eine **iwmperroritem** -Schnittstelle ab, wenn das Medien Element einen Fehlerzustand aufweist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib. iwmperroritem** -Schnittstelle, die Zugriff auf Informationen über den Fehlerzustand bereitstellt.

## <a name="remarks"></a>Bemerkungen

Wenn das Medien Element nicht wiedergegeben werden kann, ruft diese Eigenschaft eine **iwmperroritem** -Schnittstelle ab, die Informationen über das aufgetretene Problem enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmperroritem (VB und c#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPMedia2-Schnittstelle (VB und c#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





