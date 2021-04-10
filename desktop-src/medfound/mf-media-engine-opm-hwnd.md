---
description: Gibt ein Fenster an, in dem die Medien-Engine den OPM-Schutz (Output Protection Manager) anwenden soll.
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961129"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>\_ \_ \_ OPM- \_ HWND-Attribut der MF-Medien-Engine

Gibt ein Fenster an, in dem die Medien-Engine den OPM-Schutz ( [Output Protection Manager](output-protection-manager.md) ) anwenden soll.

## <a name="data-type"></a>Datentyp

**HWND** als **UINT64** gespeichert

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.

Um den OPM-Schutz für die Videowiedergabe zu aktivieren, muss die Anwendung einen der folgenden Schritte ausführen:

-   Legen Sie [das \_ \_ \_ \_ HWND](mf-media-engine-playback-hwnd.md) -Attribut der MF-Medien-Engine beim Erstellen der Medien-Engine fest.
-   Legen Sie \_ \_ \_ \_ beim Erstellen der Medien-Engine das OPM-HWND-Attribut der MF-Medien-Engine fest
-   Nach dem Erstellen der Medien-Engine, aber vor dem Anzeigen geschützter Inhalte, muss [**imfmediaengineprotectedcontent::**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) Setup-Window aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>MF mediaengine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medien-Engine-Attribute](media-engine-attributes.md)
</dt> </dl>

 

 




