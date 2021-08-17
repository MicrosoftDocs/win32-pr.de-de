---
description: Gibt an, ob die ASF-Medienquelle ungefähre Suchmöglichkeiten verwendet.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f68dedbf2b008870021e620029a039c21465d4bb45a23428225d7c88fae6583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874334"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>MFPKEY \_ ASFMediaSource \_ ApproxSeek (Eigenschaft)

Gibt an, ob die ASF-Medienquelle ungefähre Suchmöglichkeiten verwendet.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Hinweise

Anwendungen können diese Eigenschaft verwenden, um die ASF-Medienquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Die ASF-Medienquelle verarbeitet suchte wie folgt:

-   Wenn der Wert dieser Eigenschaft **VARIANT \_ TRUE** ist, verwendet die Medienquelle eine ungefähre Suche, die weniger genau, aber schneller als die genaue Suche ist.
-   Wenn der Wert **VARIANT \_ FALSE ist** und die ASF-Datei über einen Index verfügt, verwendet die Medienquelle genaue Suchmöglichkeiten.
-   Wenn die ASF-Datei keinen Index enthält, verwendet die Medienquelle camate seeking, es sei denn, die [ \_ \_ IterativeSeekIfNoIndex-Eigenschaft von MFPKEY ASFMediaSource](mfpkey-asfmediasource-iterativeseekifnoindex.md) ist auf **VARIANT TRUE \_ festgelegt.**
-   Wenn die ASF-Datei keinen Index enthält und die [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex-Eigenschaft](mfpkey-asfmediasource-iterativeseekifnoindex.md) **VARIANT \_ TRUE** ist, verwendet die Medienquelle iterative Suchmöglichkeiten. Die iterative Suche ist genauer, aber langsamer als die ungefähre Suche (aber im Allgemeinen weniger genau als die genaue Suche).
    > [!Note]  
    > Erfordert Windows 7.

     

Der Standardwert dieser Eigenschaft ist **VARIANT \_ FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




