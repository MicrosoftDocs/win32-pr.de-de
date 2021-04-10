---
description: Media Foundation Makros
ms.assetid: c460b1cd-13d7-4b65-a755-23b2ea87864d
title: Media Foundation Makros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bed83710f41957edc1b945fecd5d68b5550b4ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961108"
---
# <a name="media-foundation-macros"></a>Media Foundation Makros

## <a name="in-this-section"></a>In diesem Abschnitt



| Attribut                                                                                              | BESCHREIBUNG                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_mediaType- \_ GUID definieren**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid)<br/>                              | Definiert eine GUID für den Medien Untertyp aus einem FourCC-Code, einem **D3DFORMAT** -Wert oder einem audioformattyp.<br/>                                                                       |
| [**MFP \_ get \_ \_ User \_ Credential- \_ Ereignis abrufen**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event)<br/> | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP- \_ \_ \_ \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event) Zeiger zum Abrufen von Benutzer Anmelde Informationen um.<br/> |
| [**MFP \_ get \_ Error- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event)<br/>                                       | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP- \_ Fehler \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_error_event) Zeiger um.<br/>                                       |
| [**MFP \_ get \_ Frame \_ Step- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_frame_step_event)<br/>                            | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger auf einen [**MFP-Frame- \_ \_ \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_frame_step_event) Zeiger um.<br/>                            |
| [**MFP \_ get \_ mediaitem \_ - \_ Ereignis gelöscht**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_cleared_event)<br/>              | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen von [**mediaitem \_ gelöschten \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_cleared_event) Zeiger um.<br/>                   |
| [**MFP \_ get \_ mediaitem \_ created- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event)<br/>              | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger auf einen Ereignis Zeiger, der von [**MFP \_ mediaitem \_ erstellt wurde \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_created_event) , um.<br/>              |
| [**MFP \_ get \_ mediaitem \_ Set- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event)<br/>                      | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen Ereignis Zeiger für einen [**MFP- \_ mediaitem- \_ Satz \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event) um.<br/>                      |
| [**MFP \_ get \_ MF- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event)<br/>                                             | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP-MF- \_ \_ Ereignis**](/windows/win32/api/mfplay/ns-mfplay-mfp_mf_event) Zeiger um.<br/>                                              |
| [**MFP- \_ get- \_ Pause- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_pause_event)<br/>                                       | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger auf einen [**MFP-Ereignis Zeiger zum Anhalten des \_ \_ Ereignisses**](/windows/desktop/api/mfplay/ns-mfplay-mfp_pause_event) um.<br/>                                       |
| [**MFP \_ get \_ Play- \_ Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event)<br/>                                         | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP- \_ Wiedergabe \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) Zeiger um.<br/>                                         |
| [**MFP \_ - \_ \_ Ereignis zum Beenden der Wiedergabe \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event)<br/>                    | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen Ereignis Zeiger für den [**MFP- \_ Wiedergabe \_ \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_playback_ended_event) um.<br/>                    |
| [**MFP- \_ Ereignis für get- \_ Positions \_ Satz \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_position_set_event)<br/>                        | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP- \_ Positions \_ Satz \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event) Zeiger um.<br/>                        |
| [**MFP \_ - \_ Ereignis Get Rate \_ Set \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event)<br/>                                | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP- \_ Satz \_ \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_rate_set_event) Zeiger um.<br/>                                |
| [**MFP \_ get \_ - \_ Ereignis zum Abbrechen**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_stop_event)<br/>                                         | Wandelt einen [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in einen [**MFP-Ereignis Zeiger für das \_ Beenden \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event) um.<br/>                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> </dl>

 

 
