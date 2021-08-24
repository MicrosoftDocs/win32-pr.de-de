---
description: Media Foundation Makros
ms.assetid: c460b1cd-13d7-4b65-a755-23b2ea87864d
title: Media Foundation Makros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53a0ebbc8da6f9f65b9c8167097f4150457a6e6cbcbefe0db45032eb55d57000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724080"
---
# <a name="media-foundation-macros"></a>Media Foundation Makros

## <a name="in-this-section"></a>In diesem Abschnitt



| attribute                                                                                              | Beschreibung                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEFINIEREN \_ DER \_ MEDIATYPE-GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid)<br/>                              | Definiert eine Medienuntertyp-GUID aus einem FOURCC-Code, **einem D3DFORMAT-Wert** oder einem Audioformattyp.<br/>                                                                       |
| [**MFP \_ GET \_ ACQUIRE \_ USER \_ CREDENTIAL \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event)<br/> | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MFP ACQUIRE USER \_ \_ \_ CREDENTIAL \_ EVENT pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event)<br/> |
| [**MFP \_ GET \_ ERROR \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event)<br/>                                       | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MFP ERROR EVENT \_ \_ pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_error_event)<br/>                                       |
| [**MFP \_ GET \_ FRAME \_ STEP \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_frame_step_event)<br/>                            | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MFP FRAME STEP EVENT \_ \_ \_ pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_frame_step_event)<br/>                            |
| [**MFP \_ GET \_ MEDIAITEM \_ CLEARED \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_cleared_event)<br/>              | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MEDIAITEM \_ CLEARED EVENT \_ pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_cleared_event)<br/>                   |
| [**MFP \_ GET \_ MEDIAITEM \_ CREATED \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event)<br/>              | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MFP \_ MEDIAITEM \_ CREATED EVENT \_ pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_created_event)<br/>              |
| [**MFP \_ GET \_ MEDIAITEM \_ SET \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event)<br/>                      | Setzt einen [**\_ MFP-EREIGNISHEADerzeiger \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in einen [**MFP \_ MEDIAITEM \_ SET \_ EVENT-Zeiger**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event) um.<br/>                      |
| [**MFP \_ GET \_ MF \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event)<br/>                                             | Gibt einen [**\_ MFP-EREIGNISHEADerzeiger \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in einen [**MFP \_ \_ MF-EREIGNISzeiger**](/windows/win32/api/mfplay/ns-mfplay-mfp_mf_event) um.<br/>                                              |
| [**MFP \_ GET \_ PAUSE \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_pause_event)<br/>                                       | Gibt einen [**\_ MFP-EREIGNISHEADerzeiger \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in einen [**MFP \_ PAUSE \_ EVENT-Zeiger**](/windows/desktop/api/mfplay/ns-mfplay-mfp_pause_event) um.<br/>                                       |
| [**MFP \_ GET \_ PLAY \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event)<br/>                                         | Gibt einen [**\_ MFP-EREIGNISHEADerzeiger \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in einen [**MFP \_ \_ PLAY-EREIGNISzeiger**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) um.<br/>                                         |
| [**MFP \_ GET \_ PLAYBACK \_ ENDED \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event)<br/>                    | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MFP PLAYBACK ENDED EVENT \_ \_ \_ pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_playback_ended_event)<br/>                    |
| [**MFP \_ GET \_ POSITION \_ SET \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_position_set_event)<br/>                        | Casts an [**MFP \_ EVENT HEADER \_ pointer**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) to an [**MFP POSITION SET EVENT \_ \_ \_ pointer.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event)<br/>                        |
| [**MFP \_ GET \_ RATE \_ SET \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event)<br/>                                | Setzt einen [**\_ MFP-EREIGNISHEADerzeiger \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in einen [**MFP \_ RATE \_ \_ SET-EREIGNISzeiger**](/windows/desktop/api/mfplay/ns-mfplay-mfp_rate_set_event) um.<br/>                                |
| [**MFP \_ GET \_ STOP \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_stop_event)<br/>                                         | Gibt einen [**\_ MFP-EREIGNISHEADerzeiger \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in einen [**MFP \_ STOP \_ EVENT-Zeiger**](/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event) um.<br/>                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> </dl>

 

 
