---
description: Die PKEY \_ AudioEngine \_ OEMFormat-Eigenschaft gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed43ee7a607bc7b97e6ce521c3c1f76356380d27b3471d16dde27cd021838e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053640"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ AudioEngine \_ OEMFormat

Die PKEY \_ AudioEngine \_ OEMFormat-Eigenschaft gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT-BLOB \_ festgelegt.

Der **Blobmember** der **PROPVARIANT-Struktur** ist eine Struktur vom Typ **BLOB,** die zwei Member enthält. Member **blob.cbSize** ist ein **DWORD,** das die Anzahl der Bytes in der Formatbeschreibung angibt. Member **blob.pBlobData** zeigt auf eine **WAVEFORMATEX-Struktur,** die die Formatbeschreibung enthält. Weitere Informationen zu BLOB finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu **WAVEFORMATEX** finden Sie in der Windows DDK-Dokumentation.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




