---
description: Die Eigenschaft "pkey \_ Audioengine \_ oemformat" gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127428"
---
# <a name="pkey_audioengine_oemformat"></a>Pkey \_ Audioengine- \_ oemformat

Die Eigenschaft "pkey \_ Audioengine \_ oemformat" gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf einen VT- \_ BLOB festgelegt.

Der **BLOB** -Member der **PROPVARIANT** -Struktur ist eine Struktur vom Typ " **BLOB** ", die zwei Member enthält. Member **BLOB. cbSize** ist ein **DWORD** -Wert, der die Anzahl der Bytes in der Formatbeschreibung angibt. Member **BLOB. pblobdata** verweist auf eine **WaveFormatEx** -Struktur, die die Formatbeschreibung enthält. Weitere Informationen zum BLOB finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu **WaveFormatEx** finden Sie in der Windows-DDK-Dokumentation.

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

 

 




