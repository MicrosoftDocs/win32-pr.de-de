---
description: Gibt an, welcher Stream ein Aufzeichnungs Ereignis generiert hat.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863596"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a>Daten \_ \_ Strom- \_ \_ \_ Index Attribut für das MF-Erfassungs Modul

Gibt an, welcher Stream ein Aufzeichnungs Ereignis generiert hat.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für einige Ereignisse der Aufzeichnungs-Engine angezeigt. Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) für das Ereignis Objekt. Das Ereignis Objekt wird über die [**imfcaptureengineoneventcallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) -Methode an die Anwendung übermittelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>"MF"-Engine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMF captureengineoneventcallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




