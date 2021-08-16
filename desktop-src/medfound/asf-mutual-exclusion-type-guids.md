---
description: Die folgenden GUIDs definieren die Typen für das Objekt für gegenseitigen Ausschluss für ASF-Streams (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: ASF-GUIDs für gegenseitigen Ausschluss (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fc035248610c8f58928347093dad4470f58f9818dc99fee1d88ac3fc0d13d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035538"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUIDs des gegenseitigen ASF-Ausschlusstyps

Die folgenden GUIDs definieren die Typen für das Objekt für gegenseitigen Ausschluss für ASF-Streams (Advanced Systems Format).



| Konstante                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**MFASFMutexType-Sprache \_**</dt> </dl>                 | Die Datenströme schließen sich durch die Sprache gegenseitig aus. Diese Art des gegenseitigen Ausschlusses ähnelt den Audiospuren auf einer DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**MFASFMutexType-Bitrate \_**</dt> </dl>                     | Die Streams schließen sich durch die Bitrate gegenseitig aus. Diese Art von gegenseitigem Ausschluss wird auch als MBR-Ausschluss (Multiple Bit Rate) bezeichnet.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**MFASFMutexType-Präsentation \_**</dt> </dl> | Die Streams schließen sich durch Darstellung gegenseitig aus. Dieser Typ kann für viele Szenarien verwendet werden. Er sollte jedoch nur verwendet werden, wenn der Inhalt identisch ist, aber eine andere Form hat. Beispielsweise sollten zwei Streams, die dasselbe Video enthalten, einen, der zum Füllen des Bildschirms formatiert ist, und der andere, der das ursprüngliche Seitenverhältnis des Widescreens beibeinhaltet, sich mit diesem Typ gegenseitig ausschließen. Ein weiteres Beispiel sind Streams, die Videos derselben Szene enthalten, die aus verschiedenen Winkeln gedreht wurden.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ Unbekannt**</dt> </dl>                     | Die Streams schließen sich basierend auf benutzerdefinierten Kriterien gegenseitig aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMFASFMutualExclusion::GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> </dl>

 

 




