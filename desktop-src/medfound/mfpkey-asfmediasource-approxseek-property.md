---
description: Gibt an, ob die ASF-Medienquelle die ungefähre Suche verwendet.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106349774"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>Mfpkey \_ asfmediasource \_ approxseek (Eigenschaft)

Gibt an, ob die ASF-Medienquelle die ungefähre Suche verwendet.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Variant \_ bool**

VT \_ bool

**Boolesche Werte**



## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft verwenden, um die ASF-Medienquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Die ASF-Medienquelle behandelt die Suche wie folgt:

-   Wenn der Wert dieser Eigenschaft **Variant \_ true** ist, verwendet die Medienquelle die ungefähre Suche, die weniger genau, aber schneller als die genaue Suche ist.
-   Wenn der Wert **Variant \_ false** ist und die ASF-Datei über einen Index verfügt, verwendet die Medienquelle die genaue Suche.
-   Wenn die ASF-Datei keinen Index enthält, verwendet die Medienquelle die approxmate-Suche, es sei denn, die Eigenschaft " [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md) " ist auf **Variant \_ true** festgelegt.
-   Wenn die ASF-Datei keinen Index enthält und die Eigenschaft [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md) den Wert **Variant \_ true** hat, verwendet die Medienquelle iteratives suchen. Das iterative suchen ist präziser, aber langsamer als die ungefähre Suche (in der Regel weniger genau als bei der exakten Suche).
    > [!Note]  
    > Erfordert Windows 7.

     

Der Standardwert dieser Eigenschaft ist **Variant \_ false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




