---
title: Iwmpclosedcaption-captioningid (Eigenschaft)
description: Die iwmpclosedcaption-Eigenschaft ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt diesen fest.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- captioningid-Eigenschaft, Fenster Media Player
- captioningid-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, captioningid (Eigenschaft)
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
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358601"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>Iwmpclosedcaption:: captioningid (Eigenschaft)

Die **iwmpclosedcaption** -Eigenschaft ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die **System. String** -ID, die die ID des HTML-Elements ist.

## <a name="remarks"></a>Bemerkungen

Der angegebene Elementname kann ein beliebiges HTML-Element auf der Webseite sein, solange es das **InnerHtml** -Attribut unterstützt. Wenn die Webseite mehrere Frames enthält, kann der Elementname nur auf ein Element im gleichen Frame wie das Windows Media Player-Steuerelement verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





