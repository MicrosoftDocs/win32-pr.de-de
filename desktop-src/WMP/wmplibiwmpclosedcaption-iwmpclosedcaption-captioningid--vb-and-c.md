---
title: IWMPClosedCaption captioningId-Eigenschaft
description: Die IWMPClosedCaption-Eigenschaft ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt den Namen fest.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- captioningId-Eigenschaft Windows Media Player
- captioningId-Eigenschaft Windows Media Player , IWMPClosedCaption-Schnittstelle
- IWMPClosedCaption-Schnittstelle Windows Media Player , captioningId-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f6d4c10beb3f0fd94da0365d67b6c5ab480d36d5a3786021f538e9dcf4e90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116056"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>IWMPClosedCaption::captioningId-Eigenschaft

Die **IWMPClosedCaption-Eigenschaft** ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt den Namen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die **System.String,** die die ID des HTML-Elements ist.

## <a name="remarks"></a>Hinweise

Der angegebene Elementname kann ein beliebiges HTML-Element auf der Webseite sein, solange er das **innerHTML-Attribut** unterstützt. Wenn die Webseite mehrere Frames enthält, kann der Elementname nur auf ein Element im selben Frame verweisen wie das Windows Media Player-Steuerelement.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





