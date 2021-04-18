---
description: Diese Eigenschaft fragt den Decoder nach der maximalen voll Bild Rate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine "am \_ queryrate"-Struktur.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371427"
---
# <a name="am_rate_queryfullframerate-property"></a>Der \_ Rate der \_ queryfullframerate-Eigenschaft

Diese Eigenschaft fragt den Decoder nach der maximalen voll Bild Rate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine " **am \_ queryrate** "-Struktur.

Diese Eigenschaft ist für die Version 1,1 dieser Eigenschaften Gruppe definiert. Weitere Informationen finden Sie unter [**\_ Rate \_ userateversion**](am-rate-userateversion-property.md).



|                   |                                       |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropltid \_         |
| Eigenschafts-ID       | Der \_ Rate der \_ queryfullframerate-Eigenschaft |
| Datentyp         | [**AM- \_ querytrate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Wiedergabe Rate die maximale Rate des Decoders überschreitet, sendet der Quell Filter Gruppen von kontinuierlichen Samplings, die durch Diskontinuitäten getrennt sind. Die Zeitstempel überspringen die Diskontinuitäten. Der Quell Filter kann dies auch dann tun, wenn die Wiedergabe Rate innerhalb der maximalen Rate des Decoders liegt, da es möglicherweise andere Faktoren gibt, wie z. b. Datenträger-e/a, die die vollständige Wiedergabe Rate einschränken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md)
</dt> </dl>

 

 




