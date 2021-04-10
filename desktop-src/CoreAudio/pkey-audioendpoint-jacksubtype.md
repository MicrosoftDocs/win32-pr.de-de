---
description: Die Eigenschaft "pkey \_ audioendpoint \_ jacksubtype" enthält eine Ausgabe Kategorie-GUID für ein audioendpunktgerät.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127437"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>Pkey- \_ audioendpoint-" \_ jacksubtype"

Die Eigenschaft " **pkey \_ audioendpoint \_ jacksubtype** " enthält eine Ausgabe Kategorie-GUID für ein audioendpunktgerät. Die Header Datei "ksmedia. h" definiert die GUIDs. jeder GUID gibt den Verbindungstyp an. Diese GUIDs verfügen auch über zugehörige Pin-Kategorien. Die Header Datei "ksmedia. h" definiert z. b. die GUID **ksnodetype \_ DisplayPort- \_ Schnittstelle** für einen anzeigeport, der eine Verbindung mit der von der GUID **Pinname \_ DisplayPort \_ out** definierten KS-Pin herstellt.

Weitere Informationen finden Sie in der Beschreibung der Eigenschaften der PIN-Kategorie in der Windows-DDK-Dokumentation.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf **VT \_ LPWSTR** festgelegt.

Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine Kategorie-GUID enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften des audioendpunkts**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




