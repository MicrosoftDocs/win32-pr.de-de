---
description: Diese Klasse ist die übergeordnete Klasse für Image-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Image-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979872"
---
# <a name="image-class"></a>Image-Klasse

Diese Klasse ist die übergeordnete Klasse für Image-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Image** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um Bild Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Ablaufverfolgungsflag für das Ereignis Ablaufverfolgungsflag im **enableflags** -Member der Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion **\_ \_ \_ \_**

Ereignisablaufverfolgungslistener können eine spezielle Verarbeitung für Bild Lade Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**imageloadguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um Bild Lade Ereignisse beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                          | BESCHREIBUNG                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ \_ \_ Laden von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 10)<br/>     | Bild Lade Ereignis. Wird generiert, wenn eine DLL oder eine ausführbare Datei geladen wird. Der Anbieter generiert nur ein Ereignis zum ersten Mal, wenn eine bestimmte dll geladen wird. Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.      |
| **Ereignis \_ Ablaufverfolgungstyp \_ \_ Ende**(Ereignistyp Wert ist 2)<br/>       | Bild Entlade Ereignis. Wird generiert, wenn eine DLL oder eine ausführbare Datei entladen wird. Der Anbieter generiert nur ein Ereignis für den letzten Zeitpunkt, an dem eine bestimmte DLL entladen wird. Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis. |
| **Ereignis \_ Ablauf Verfolgungs \_ Typen- \_ DC- \_ Start**(Ereignistyp Wert ist 3)<br/> | Start Ereignis für die Datensammlung. Listet alle geladenen Bilder am Anfang der Ablauf Verfolgung auf. Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| **Ereignis \_ Trace- \_ Typ- \_ DC- \_ Ende**(Ereignistyp Wert ist 4)<br/>   | Ereignis zum Beenden der Datensammlung. Listet alle geladenen Bilder am Ende der Ablauf Verfolgung auf. Die MOF-Klasse " [**Image \_ Load**](image-load.md) " definiert die Ereignisdaten für dieses Ereignis.                                                                          |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**Laden von Bildern \_**](image-load.md)
</dt> <dt>

[**Bild \_ v0**](image-v0.md)
</dt> <dt>

[**Bild \_ v1**](image-v1.md)
</dt> </dl>

 

 
