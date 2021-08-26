---
description: Die PKEY \_ AudioEndpoint \_ JackSubType-Eigenschaft enthält eine Ausgabekategorie-GUID für ein Audioendpunktgerät.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95ca24d48a35299144f36d052ceea2e2d0d12c56fbc03b58a993fd95772c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053730"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

Die **PKEY \_ AudioEndpoint \_ JackSubType-Eigenschaft** enthält eine Ausgabekategorie-GUID für ein Audioendpunktgerät. Die Headerdatei Ksmedia.h definiert die GUIDs. Jede GUID gibt den Verbindungstyp an. Diesen GUIDs sind auch Pinkategorien zugeordnet. Beispielsweise definiert die Headerdatei Ksmedia.h die GUID **KSNODETYPE \_ DISPLAYPORT \_ INTERFACE** für einen Anzeigeport, der eine Verbindung mit dem KS-Pin herstellt, der durch die GUID **PINNAME \_ DISPLAYPORT \_ OUT definiert ist.**

Weitere Informationen finden Sie in der Beschreibung der Eigenschaften der Stecknadelkategorie in der Windows DDK-Dokumentation.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf **VT \_ LPWSTR festgelegt.**

Der **pwszVal-Member** der **PROPVARIANT-Struktur** zeigt auf eine null terminierte Breitzeichenzeichenfolge, die eine Kategorie-GUID enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




