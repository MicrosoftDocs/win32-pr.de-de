---
description: Die pkey \_ audioendpoint \_ -Zuordnungs Eigenschaft ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345634"
---
# <a name="pkey_audioendpoint_association"></a>Pkey \_ audioendpoint-Zuordnung \_

Die **pkey \_ audioendpoint \_** -Zuordnungs Eigenschaft ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu. Die INF-Datei, mit der ein Audioadapter installiert wird, weist jeder anheft-PIN im Adapter eine PIN-Kategorie zu. Eine anheft-PIN auf einem Adapter Gerät stellt den Punkt dar, an dem ein Audiostream das Gerät betritt oder verlässt. Eine PIN-Kategorie ist eine GUID, die den Typ der von einer Pin-Pin ausgeführten Funktion angibt. Die Header Datei "ksmedia. h" definiert z. b. die PIN-Kategorie GUID ksnodetype \_ Mikrofon, um eine KS-PIN anzugeben, die mit einem Mikrofon verbunden ist, und ksnodetype- \_ Kopfhörer, um eine KS-PIN anzugeben, die eine Verbindung mit dem Weitere Informationen finden Sie in der Beschreibung der Eigenschaften der PIN-Kategorie in der Windows-DDK-Dokumentation.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.

Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine-PIN-Kategorie-GUID enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften des audioendpunkts**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




