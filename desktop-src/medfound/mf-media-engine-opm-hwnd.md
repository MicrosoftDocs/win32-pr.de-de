---
description: Gibt ein Fenster an, in dem die Medien-Engine OPM-Schutz (Output Protection Manager) anwenden kann.
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND -Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1079e7b9503c73ea678e4f9fd3642ec94fe43a1326e6f33a635f81d1bc1a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013070"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>OPM \_ \_ \_ \_ HWND-Attribut der MF-MEDIEN-ENGINE

Gibt ein Fenster an, in dem die Medien-Engine OPM-Schutz [(Output Protection Manager)](output-protection-manager.md) anwenden kann.

## <a name="data-type"></a>Datentyp

**HWND als** **UINT64 gespeichert**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird zusammen mit der [**METHODE FÜR DIETMEDIAEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) verwendet, um die Medien-Engine zu initialisieren.

Um OPM-Schutz für die Videowiedergabe zu aktivieren, muss die Anwendung einen der folgenden Schritte unternehmen:

-   Legen Sie das [MF \_ MEDIA ENGINE PLAYBACK \_ \_ \_ HWND-Attribut](mf-media-engine-playback-hwnd.md) fest, wenn Sie die Medien-Engine erstellen.
-   Legen Sie das MF \_ MEDIA \_ ENGINE \_ OPM \_ HWND-Attribut fest, wenn Sie die Medien-Engine erstellen.
-   Rufen [**Sie ZU jedem Zeitpunkt NACH**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) dem Erstellen der Medien-Engine, aber bevor geschützter Inhalt angezeigt wird, DEN AUFRUF ZU EINEM BELIEBIGEN ZEITPUNKT AUF.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medien-Engine-Attribute](media-engine-attributes.md)
</dt> </dl>

 

 




