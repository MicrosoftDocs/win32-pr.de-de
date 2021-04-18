---
description: Gesendet von der Pipeline an Encoder-MFTs serialisiert mit Medien Beispielen über imftransform::P rocesabvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Meencodingparameters-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215170"
---
# <a name="meencodingparameters-event"></a>Meencodingparameters-Ereignis

Gesendet von der Pipeline an Encoder-MFTs serialisiert mit Medien Beispielen über [**imftransform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                         | BESCHREIBUNG                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | Enthält die neuen icodecapi-basierten Einstellungen, die der Encoder auf nachfolgende eingehende Stichproben anwenden soll.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Ereignis Nutzlast ist ein Attribut Speicher (imfattributes-Zeiger), der die neuen icodecapi-basierten///-Einstellungen enthält, die der Encoder auf nachfolgende eingehende Beispiele anwenden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




