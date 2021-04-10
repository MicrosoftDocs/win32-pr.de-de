---
description: Die folgenden GUIDs definieren die Typen für das gegenseitige Ausschluss Objekt für ASF-Streams (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: Gegenseitige ASF-Ausschluss Typen-GUIDs (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214345"
---
# <a name="asf-mutual-exclusion-type-guids"></a>Gegenseitige ASF-Ausschluss Typen-GUIDs

Die folgenden GUIDs definieren die Typen für das gegenseitige Ausschluss Objekt für ASF-Streams (Advanced Systems Format).



| Konstante                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**Mfasf mutextype- \_ Sprache**</dt> </dl>                 | Die Streams schließen sich gegenseitig aus. Diese Art des gegenseitigen Ausschlusses ähnelt den Audiospuren auf einer DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**Mfasf mutextype- \_ Bitrate**</dt> </dl>                     | Die Streams schließen sich durch die Bitrate gegenseitig aus. Diese Art des gegenseitigen Ausschlusses wird auch als MBR-Ausschluss (Multiple Bitrate) bezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Mfasf mutextype- \_ Präsentation**</dt> </dl> | Die Streams schließen sich gegenseitig aus. Dieser Typ kann für viele Szenarien verwendet werden, sollte jedoch nur verwendet werden, wenn der Inhalt identisch ist, aber eine andere Form hat. Beispielsweise sollten zwei Datenströme, die das gleiche Video enthalten, eine formatiert, um den Bildschirm zu füllen, und die andere Datenströme, die das ursprüngliche Widescreen-Seitenverhältnis behalten, mithilfe dieses Typs gegenseitig ausschließen werden. Ein weiteres Beispiel sind Datenströme, die Videos aus unterschiedlichen Winkeln mit dem gleichen Szenenfoto enthalten.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**Mfasf mutextype \_ unbekannt**</dt> </dl>                     | Die Streams schließen sich basierend auf den benutzerdefinierten Kriterien gegenseitig aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfassmutualexclusion:: GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**Imfassmutualexclusion:: settype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> </dl>

 

 




