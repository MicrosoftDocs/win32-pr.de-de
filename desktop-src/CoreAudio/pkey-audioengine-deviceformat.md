---
description: Die PKEY \_ AudioEngine \_ DeviceFormat-Eigenschaft gibt das Geräteformat an. Dabei handelt es sich um das Format, das der Benutzer für den Datenstrom ausgewählt hat, der zwischen der Audio-Engine und dem Audioendpunktgerät fließt, wenn das Gerät im freigegebenen Modus betrieben wird.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13245d23095c25173a894a7a4c7cc11b2cdc534f6ae7198508b725d0fd1cf0b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018328"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ AudioEngine \_ DeviceFormat

Die **PKEY \_ AudioEngine \_ DeviceFormat-Eigenschaft** gibt das Geräteformat an. Dabei handelt es sich um das Format, das der Benutzer für den Datenstrom ausgewählt hat, der zwischen der Audio-Engine und dem Audioendpunktgerät fließt, wenn das Gerät im freigegebenen Modus betrieben wird. Dieses Format ist möglicherweise nicht das beste Standardformat für eine Anwendung im exklusiven Modus. In der Regel findet eine Anwendung im exklusiven Modus ein geeignetes Geräteformat, indem einige Aufrufe an die [**IAudioClient::IsFormatSupported-Methode ausgeführt werden.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) Weitere Informationen finden Sie unter [Geräteformate.](device-formats.md)

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT-BLOB \_ festgelegt.

Der **Blobmember** der **PROPVARIANT-Struktur** ist eine Struktur vom Typ **BLOB,** die zwei Member enthält. Member **blob.cbSize** ist ein **DWORD,** das die Anzahl der Bytes in der Formatbeschreibung angibt. Member **blob.pBlobData** zeigt auf eine **WAVEFORMATEX-Struktur,** die die Formatbeschreibung enthält. Weitere Informationen zu BLOB finden Sie in der Windows **SDK-Dokumentation.** Weitere Informationen zu **WAVEFORMATEX** finden Sie in der Windows DDK-Dokumentation.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




