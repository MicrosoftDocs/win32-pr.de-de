---
description: Gibt die Grenzen des relevanten Bereichs an, der den Bereich des Frames angibt, der unterschiedliche Qualität erfordert.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356891"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>MF Sample Extension- \_ Attribut (roirechteck)

Gibt die Grenzen des relevanten Bereichs an, der den Bereich des Frames angibt, der unterschiedliche Qualität erfordert.

## <a name="data-type"></a>Datentyp

**[**ROI \_**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** Als **BLOB** gespeicherter Bereich

## <a name="remarks"></a>Bemerkungen

Nach der erfolgreichen Festlegung von [codecapi \_ avencvideoroiaktiviertem](codecapi-avencvideoroienabled.md) Wert ungleich 0 (null) auf einem Encoder-MFT kann die Anwendung dieses Attribut für Eingabe Beispiele festlegen und erwarten, dass Sie berücksichtigt werden.

Wenn [codecapi \_ avencvideoroiaktivinicht](codecapi-avencvideoroienabled.md) auf einen Wert ungleich 0 (null) festgelegt ist, wird das Attribut "mfsampleextension \_ roirechteck" bei Eingabe Beispielen ignoriert.

Das mfsampleextension \_ -roirechteck ist für ein Eingabe Beispiel festgelegt und wird nur auf das aktuelle Eingabe Beispiel angewendet.

Das Feld **qpdelta** in der [**ROI- \_ Bereichs**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) Struktur gibt den quantisierungsparameterdelta für den angegebenen Bereich vom Rest des Frames an. Wenn **qpdelta** positiv ist, bedeutet dies, dass die Anwendung für das Rechteck eine niedrigere Qualität als für den Rest des Frames hat.

**H. 264/AVC-Encoder:** **qpdelta** muss zwischen \[ -25 und + 25 liegen \] . Der Encoder muss sicherstellen, dass das endgültige QP in einem gültigen Bereich für den Videostandard liegt.

Der angegebene Bereich muss nicht auf MB ausgerichtet sein. Encoder können die tatsächliche Grenze flexibel festlegen. Es wird empfohlen, den gesamten angegebenen Bereich abzudecken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




