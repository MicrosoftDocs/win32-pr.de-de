---
description: Aktiviert oder deaktiviert den Read-Ahead-Vorgang in einer Medienquelle.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: MFPKEY_MediaSource_DisableReadAhead-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359377"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>Eigenschaft "mfpkey \_ MediaSource \_ disablereadahead"

Aktiviert oder deaktiviert den Read-Ahead-Vorgang in einer Medienquelle.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Variant \_ bool**

VT \_ bool

**Boolesche Werte**



## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft verwenden, um einige Medienquellen zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Wenn der Wert **Variant \_ true** ist, wird die Medienquelle nicht im Bytestream eingelesen. Diese Einstellung kann die Leistung optimieren, wenn Sie eine begrenzte Menge von Daten aus der Medienquelle lesen möchten, z. –. um ein Miniaturbild aus einer Videodatei zu erhalten.

Für eine typische Audiowiedergabe und Videowiedergabe sollte diese Eigenschaft auf **Variant \_ false** festgelegt werden. Der Standardwert ist **Variant \_ false**.

Nicht jede Medienquelle unterstützt diese Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Client<br/> | Windows 7<br/>                                                               |
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




