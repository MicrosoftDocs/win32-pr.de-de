---
description: Dieser Abschnitt enthält Informationen zu den von DXGI bereitgestellten Enumerationen.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: DXGI-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9347fdf39f2cde6bb50e3ae4c65f2601c570e084516bf817c4dc66169a83925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987140"
---
# <a name="dxgi-enumerations"></a>DXGI-Enumerationen

Dieser Abschnitt enthält Informationen zu den von DXGI bereitgestellten Enumerationen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                         | Beschreibung                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ DXGI-ADAPTERFLAG**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifiziert den Typ des DXGI-Adapters.<br/>                                                                                                                                   |
| [**\_ \_ DXGI-ADAPTERFLAG3**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifiziert den Typ des DXGI-Adapters.<br/>                                                                                                                                   |
| [**DXGI \_ \_ ALPHA-MODUS**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifiziert den Alphawert, das Transparenzverhalten, einer Oberfläche.<br/>                                                                                                       |
| [**DXGI \_ COLOR \_ SPACE \_ TYPE**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Gibt Farbraumtypen an.<br/>                                                                                                                                           |
| [**DXGI \_ COMPUTE \_ PREEMPTION \_ GRANULARITY**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifiziert die Granularität, mit der die Grafikprozessor (GRAPHICS Processing Unit, GPU) von der Ausführung ihrer aktuellen Computeaufgabe entfernt werden kann.<br/>                                      |
| [**DXGI \_ DEBUG \_ \_ RLO-FLAGS**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Flags, die mit [**ReportLiveObjects verwendet werden,**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) um die Menge der Informationen anzugeben, die über die Lebensdauer eines Objekts berichtet werden. <br/>                         |
| [**\_DXGI-FEATURE**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Gibt eine Reihe von Hardwarefeatures an, die bei der Überprüfung auf Featureunterstützung verwendet werden sollen.<br/>                                                                                  |
| [**\_DXGI-FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Ressourcendatenformate, einschließlich vollständig typ und typloser Formate. Eine Liste von Modifizierern am unteren Rand der Seite beschreibt die einzelnen Formattypen genauer. <br/>               |
| [**DXGI \_ FRAME \_ PRESENTATION \_ MODE**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Gibt Optionen zum Präsentieren von Frames in der Swapkette an. <br/>                                                                                                            |
| [**DXGI \_ GPU \_ PREFERENCE**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | Die Einstellung der GPU für die Ausführung der App.<br/>                                                                                                                           |
| [**DXGI \_ GRAPHICS \_ PREEMPTION \_ GRANULARITY**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifiziert die Granularität, mit der die GPU von der Ausführung ihrer aktuellen Grafikrenderingaufgabe entfernt werden kann.<br/>                                                      |
| [**DXGI \_ HARDWARE \_ COMPOSITION \_ SUPPORT \_ FLAGS**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | Beschreibt, welche Ebenen der Hardwarezusammenstellung unterstützt werden.<br/>                                                                                                          |
| [**DXGI \_ HDR \_ METADATA \_ TYPE**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Gibt den Headermetadatentyp an.<br/>                                                                                                                                    |
| [**DXGI \_ INFO \_ QUEUE \_ MESSAGE \_ CATEGORY**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Werte, die Kategorien von Debugmeldungen angeben.<br/>                                                                                                                      |
| [**DXGI \_ INFO: \_ SCHWEREGRAD DER \_ \_ WARTESCHLANGENNACHRICHT**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Werte, die den Schweregrad der Debugmeldung für eine Informationswarteschlange angeben.<br/>                                                                                            |
| [**DXGI \_ MEMORY \_ SEGMENT \_ GROUP**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Gibt die zu verwendende Speichersegmentgruppe an.<br/>                                                                                                                             |
| [**\_ \_ DXGI-MODUSROTATION**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Flags, die angeben, wie die Hintergrundpuffer gedreht werden sollen, um die physische Drehung eines Monitors zu passen.<br/>                                                                  |
| [**DXGI \_ MODE \_ SCALING**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Flags, die angeben, wie ein Bild gestreckt wird, um die Auflösung eines bestimmten Monitors zu unterstützen.<br/>                                                                                        |
| [**DXGI \_ MODE \_ SCANLINE \_ ORDER**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Flags, die die Methode angeben, mit der das Raster ein Bild auf einer Oberfläche erstellt.<br/>                                                                                           |
| [**DXGI \_ MULTIPLANE \_ OVERLAY \_ YCbCr \_ FLAGS**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Optionen für den Farbraum der Auslagerungskette.<br/>                                                                                                                                    |
| [**\_ \_ DXGI-ANGEBOTSRESSOURCENFLAGS \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Gibt Flags für die [**OfferResources1-Methode**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) an.<br/>                                                                                |
| [**\_ \_ \_ DXGI-ANGEBOTSRESSOURCENPRIORITÄT**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifiziert die Wichtigkeit des Inhalts einer Ressource, wenn Sie die [**IDXGIDevice2::OfferResources-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) aufrufen, um die Ressource anbieten zu können. <br/> |
| [**DXGI \_ OUTDUPL \_ \_ \_ ZEIGERFORMTYP**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifiziert den Typ der Zeigerform.<br/>                                                                                                                                  |
| [**DXGI \_ OVERLAY \_ COLOR \_ SPACE \_ SUPPORT \_ FLAG**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Gibt die Unterstützung für den Überlagerungsfarbraum an.<br/>                                                                                                                             |
| [**DXGI \_ OVERLAY \_ SUPPORT \_ FLAG**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Gibt die Überlagerungsunterstützung an, auf die in einem Aufruf von [**IDXGIOutput3::CheckOverlaySupport überprüft werden soll.**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport)<br/>                                     |
| [**\_DXGI– RESSOURCENERGEBNISSE \_ \_ WIEDERVERLANGEN**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Gibt Ergebnisflags für die [**ReclaimResources1-Methode**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) an.<br/>                                                                     |
| [**DXGI \_ RESIDENCY**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Flags, die den Speicherort einer Ressource angeben.<br/>                                                                                                                    |
| [**DXGI \_ SCALING**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifiziert das Größenvergrößerungsverhalten, wenn die Größe des Hintergrundpuffers nicht mit der Größe der Zielausgabe übereinstimmen soll.<br/>                                                                     |
| [**DXGI \_ SWAP \_ CHAIN \_ COLOR \_ SPACE \_ SUPPORT \_ FLAG**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Gibt die Farbraumunterstützung für die Austauschkette an.<br/>                                                                                                                      |
| [**DXGI \_ SWAP \_ CHAIN \_ FLAG**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Optionen für das Verhalten der Auslagerungskette.<br/>                                                                                                                                       |
| [**DXGI \_ SWAP \_ EFFECT**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Optionen zum Behandeln von Pixeln auf einer Anzeigeoberfläche nach dem Aufruf von [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI-Referenz](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

