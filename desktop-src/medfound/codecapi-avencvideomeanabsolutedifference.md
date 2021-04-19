---
description: Steuert das signalisieren von MF Sample Extension \_ meanabsolutedifference durch imfattribute für jedes Ausgabe Beispiel.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: CODECAPI_AVEncVideoMeanAbsoluteDifference-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345465"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>Codecapi \_ avencvideomeanabsolutedifference (Eigenschaft)

Steuert das signalisieren von [MF Sample Extension \_ meanabsolutedifference](mfsampleextension-meanabsolutedifference.md) durch [**imfattribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) für jedes Ausgabe Beispiel.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideomeanabsolutedifference**

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung einen Wert ungleich 0 (null) festlegt, sollte der Encoder jedes Ausgabe Beispiel das [mfsampleextension-Beispiel Attribut " \_ meanabsolutedifference](mfsampleextension-meanabsolutedifference.md) " hinzufügen. Das mfsampleextension- \_ Attribut "meanabsolutedifference" gibt den Mittelwert der absoluten Differenz zwischen den Quell Beispielen und den vorhergesagten Beispielen auf der Y-Ebene an.

Wenn der Encoder 0 für **getparameterrange** zurückgibt, unterstützt der Encoder die Ausgabe von [MF Sample Extension " \_ meanabsolutedifference](mfsampleextension-meanabsolutedifference.md) " nicht in den Ausgabe Beispielen.

Der Standardwert muss 0 sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




