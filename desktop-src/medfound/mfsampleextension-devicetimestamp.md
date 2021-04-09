---
description: Enthält den Zeitstempel des Gerätetreibers.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: MFSampleExtension_DeviceTimestamp-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863972"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>Devicetimestamp-Attribut für MF Sample Extension \_

Enthält den Zeitstempel des Gerätetreibers.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für Medien Beispiele festgelegt, die von einer Medienquelle für ein Erfassungsgerät erstellt wurden. Der Wert dieses Attributs ist in der [**MF-Zeit**](mftime.md) Domäne, und es wird eine Epoche mit der QPC-Zeit (Query Performance Counter) gemeinsam genutzt, die immer in 100-ns-Einheiten ausgedrückt wird Dieses Attribut ist für MFTs verfügbar, die in die Aufzeichnungs Pipeline eingefügt werden.

Um den Zeitstempel relativ zum Start des Streamings abzurufen, müssen Sie die [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) -Methode aufrufen.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoerfassung in Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> </dl>

 

 




