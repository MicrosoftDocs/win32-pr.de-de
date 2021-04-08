---
description: Gibt die Anzahl von Codierungs Durchläufen an, die der Encoder unterstützt.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Avenccommonmultipassmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860442"
---
# <a name="avenccommonmultipassmode-property"></a>Avenccommonmultipassmode (Eigenschaft)

Gibt die Anzahl von Codierungs Durchläufen an, die der Encoder unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonmultipassmode**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird als Wertebereich zurückgegeben. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Die Decodierungs Latenz ist definiert als die Menge der Daten, die der Decoder Puffern muss. Wenn Sie diese Eigenschaft beispielsweise auf **Variant \_ true** für einen MPEG-Video Encoder festlegen, werden die Typen von GOP-Strukturen, die der Encoder verwenden kann, eingeschränkt.

Um den aktuellen Codierungs Durchlauf festzulegen, legen Sie die Eigenschaft " [**avenccommonpassstart**](avenccommonpassstart-property.md) " fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




