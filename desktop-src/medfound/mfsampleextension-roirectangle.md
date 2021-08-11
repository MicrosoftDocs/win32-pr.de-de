---
description: Gibt die Begrenzungen des bereichs von Interesse an, der den Bereich des Frames angibt, der eine andere Qualität erfordert.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311b17cab20de16a83d145563e8ba0b8ead6f055428ffc6a3823c99deab05fc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240325"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>MFSampleExtension \_ ROIRectangle-Attribut

Gibt die Begrenzungen des bereichs von Interesse an, der den Bereich des Frames angibt, der eine andere Qualität erfordert.

## <a name="data-type"></a>Datentyp

**[**ROI \_ Als**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** **BLOB** gespeicherter BEREICH

## <a name="remarks"></a>Hinweise

Nach dem erfolgreichen Festlegen von [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) auf einen Wert ungleich 0 (null) in einem Encoder-MFT kann die Anwendung dieses Attribut für Eingabebeispiele festlegen und erwarten, dass es berücksichtigt wird.

Wenn [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) nicht auf einen Wert ungleich 0 (null) festgelegt ist, wird das MFSampleExtension \_ ROIRectangle-Attribut in Eingabebeispielen ignoriert.

MFSampleExtension \_ ROIRectangle wird für ein Eingabebeispiel festgelegt und nur auf das aktuelle Eingabebeispiel angewendet.

Das **QPDelta-Feld** in der [**ROI \_ AREA-Struktur**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) gibt das Delta des Quantisierungsparameters für den angegebenen Bereich aus dem restlichen Frame an. Wenn **QPDelta** positiv ist, gibt dies an, dass die Anwendung möchte, dass das Rechteck eine niedrigere Qualität als der Rest des Frames hat.

**H.264/AVC-Encoder:** **QPDelta** muss zwischen \[ -25 und +25 \] sein. Der Encoder muss sicherstellen, dass sich der endgültige QP in einem gültigen Bereich für den Videostandard befindet.

Der angegebene Bereich muss nicht mbbündig ausgerichtet sein. Encoder können flexibel über die tatsächliche Grenze entscheiden. Es wird empfohlen, die gesamte angegebene Region abzudecken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




