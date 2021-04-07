---
description: Die pkey \_ Audioengine \_ deviceformat-Eigenschaft gibt das Geräte Format an. Hierbei handelt es sich um das Format, das vom Benutzer für den Datenstrom zwischen der Audioengine und dem audioendpunktgerät ausgewählt wird, wenn das Gerät im freigegebenen Modus betrieben wird.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748904"
---
# <a name="pkey_audioengine_deviceformat"></a>Pkey \_ Audioengine \_ deviceformat

Die **pkey \_ Audioengine \_ deviceformat** -Eigenschaft gibt das Geräte Format an. Hierbei handelt es sich um das Format, das vom Benutzer für den Datenstrom zwischen der Audioengine und dem audioendpunktgerät ausgewählt wird, wenn das Gerät im freigegebenen Modus betrieben wird. Dieses Format ist möglicherweise nicht das beste Standardformat, das von einer Anwendung im exklusiven Modus verwendet werden kann. In der Regel sucht eine Anwendung im exklusiven Modus nach einem passenden Geräte Format, indem eine Reihe von Aufrufen der [**iaudioclient:: isformatsupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) -Methode ausgeführt wird. Weitere Informationen finden Sie unter [Geräte Formate](device-formats.md).

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf einen VT- \_ BLOB festgelegt.

Der **BLOB** -Member der **PROPVARIANT** -Struktur ist eine Struktur vom Typ " **BLOB** ", die zwei Member enthält. Member **BLOB. cbSize** ist ein **DWORD** -Wert, der die Anzahl der Bytes in der Formatbeschreibung angibt. Member **BLOB. pblobdata** verweist auf eine **WaveFormatEx** -Struktur, die die Formatbeschreibung enthält. Weitere Informationen zum **BLOB** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu **WaveFormatEx** finden Sie in der Windows-DDK-Dokumentation.

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

 

 




