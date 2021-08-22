---
description: Diese Klasse ist die übergeordnete Klasse für Bildereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
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
ms.openlocfilehash: a7db8595dd09790d875e502e479d14669a6df90b8de38b71fcf9ed58f2b68b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070110"
---
# <a name="image-class"></a>Image-Klasse

Diese Klasse ist die übergeordnete Klasse für Bildereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **Image-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um Bildereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG IMAGE \_ \_ \_ \_ LOAD** im **EnableFlags-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Bildladeereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ImageLoadGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um Beim Nutzen von Ereignissen Bildladeereignisse zu identifizieren.



| Ereignistyp                                                          | Beschreibung                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ LOAD**(Ereignistypwert ist 10)<br/>     | Bildladeereignis. Wird generiert, wenn eine DLL oder ausführbare Datei geladen wird. Der Anbieter generiert nur ein Ereignis, wenn eine bestimmte DLL zum ersten Mal geladen wird. Die [**\_ MOF-Klasse**](image-load.md) image load definiert die Ereignisdaten für dieses Ereignis.      |
| **EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)<br/>       | Ereignis zum Entladen von Images. Wird generiert, wenn eine DLL oder ausführbare Datei entladen wird. Der Anbieter generiert nur ein Ereignis für das letzte Entladen einer bestimmten DLL. Die [**\_ MOF-Klasse**](image-load.md) image load definiert die Ereignisdaten für dieses Ereignis. |
| **EVENT \_ TRACE \_ TYPE \_ DC \_ START**(Ereignistypwert ist 3)<br/> | Startereignis der Datensammlung. Enumeriert alle geladenen Bilder am Anfang der Ablaufverfolgung. Die [**\_ MOF-Klasse**](image-load.md) image load definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| **EVENT \_ TRACE \_ TYPE \_ DC \_ END**(Ereignistypwert ist 4)<br/>   | Endereignis der Datensammlung. Enumeriert alle geladenen Bilder am Ende der Ablaufverfolgung. Die [**\_ MOF-Klasse**](image-load.md) image load definiert die Ereignisdaten für dieses Ereignis.                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Laden von \_ Images**](image-load.md)
</dt> <dt>

[**Image \_ V0**](image-v0.md)
</dt> <dt>

[**Image \_ V1**](image-v1.md)
</dt> </dl>

 

 
