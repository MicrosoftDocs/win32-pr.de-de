---
description: Benutzerdefinierte HRESULT-Werte für die Schnittstelle zur Grafik Diagnose Erfassung.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: HRESULT-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521568"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>HRESULT-Enumeration

Benutzerdefinierte HRESULT-Werte für die Schnittstelle zur Grafik Diagnose Erfassung.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**Pix \_ S \_ OK**  
Ein gängiges HRESULT, das angibt, dass der Vorgang erwartungsgemäß erfolgreich war.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**Pix \_ S \_ false**  
Ein gängiges HRESULT, das angibt, dass der Vorgang erfolgreich war, jedoch anders als erwartet.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**Pix- \_ Fehler \_ Datei \_ nicht \_ gefunden**  
Ein benutzerdefiniertes HRESULT, dass die Fehler \_ Datei " \_ \_ .

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**Pix- \_ fehlerhafte \_ \_ Umgebung**  
Ein benutzerdefiniertes HRESULT, das auf eine ungültige Umgebung für Fehler \_ \_

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**Pix \_ - \_ Fehler \_ Format**  
Ein benutzerdefiniertes HRESULT, das ein ungültiges Format für den Fehler \_ \_

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**Pix- \_ Fehler \_ Freigabe \_ Verletzung**  
Ein benutzerdefiniertes HRESULT, bei dem die Verletzung der Fehler \_ Freigabe " \_

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**Pix-Fehler Datenträger \_ \_ \_**  
Ein benutzerdefiniertes HRESULT, das den Fehler Datenträger \_ \_ voll ist.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**Pix- \_ Fehler \_ Weitere \_ Daten**  
Ein benutzerdefiniertes HRESULT, bei dem \_ ein Fehler mit einem Fehler bei \_

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**Pix \_ E \_ fehlende \_ Debug- \_ Kits- \_ Richtlinie**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die Debug Kits-Richtlinie fehlt.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**Pix \_ E \_ ungültige \_ Version.**  
Ein benutzerdefiniertes HRESULT, das angibt, dass eine ungültige Version verwendet wird.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**Pix \_ E \_ mit \_ Dcomp**  
Ein benutzerdefiniertes HRESULT, das angibt, dass directcomposition verwendet wird (die Erfassung von directcomposition wird nicht unterstützt.)

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**Pix \_ E \_ mithilfe von \_ DirectWrite**  
Ein benutzerdefiniertes HRESULT, das angibt, dass DirectWrite verwendet wird (die Erfassung von DirectWrite wird nicht unterstützt.)

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**Pix \_ E \_ mithilfe von \_ d3d9**  
Ein benutzerdefiniertes HRESULT, das angibt, dass von Direct3D9 verwendet wird (die Erfassung von von Direct3D9 wird in Windows 10 nicht unterstützt.)

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**Pix \_ E nicht zum \_ Erstellen eines \_ \_ Shaders**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein angegebener Shader nicht erstellt werden kann.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**Pix \_ E \_ mithilfe von \_ D2D**  
Ein benutzerdefiniertes HRESULT, das angibt, dass Direct2D verwendet wird (die Erfassung von Direct2D wird nicht unterstützt.)

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**Pix \_ E \_ keine \_ Frames**  
Ein benutzerdefiniertes HRESULT, das angibt, dass keine Frames aufgezeichnet wurden.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**Pix \_ E \_ Deaktivieren von \_ Spy**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**Pix \_ E \_ WIN8LOG \_ auf \_ Win7**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein Windows 8 vsglog auf Windows 7 nicht wiedergegeben werden kann.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**Pix \_ E \_ Build- \_ Shader-Ablauf \_ Verfolgung**  
Ein benutzerdefiniertes HRESULT, das angibt, dass beim Aufbau der shaderablaufverfolgung ein Fehler aufgetreten ist.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**Pix \_ E \_ keine \_ CS- \_ Daten \_ Visualisierung**  
Ein benutzerdefiniertes HRESULT, das angibt, dass keine Datenvisualisierung für Compute-Shader vorhanden ist.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**Pix \_ E \_ Mismatch \_ SDK**  
Ein benutzerdefiniertes HRESULT, das angibt, dass das aktuelle SDK nicht übereinstimmt.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**Pix \_ E möglicherweise nicht übereinstimmende \_ \_ \_ SDK**  
Ein benutzerdefiniertes HRESULT, das angibt, dass eine mögliche Übereinstimmung mit dem aktuellen SDK vorliegt.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**Pix \_ E \_ nicht erkennbares \_ Pixel**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein nicht erkennbares Pixel vorhanden ist.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**Pix \_ E \_ cant \_ Debuggen von \_ Shader \_ mithilfe von \_ System \_ Wert \_ Semantik**  
Ein benutzerdefiniertes HRESULT, das angibt, dass der sahder nicht mithilfe der System Wert Semantik debuggten werden kann.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**Pix \_ S \_ UpdateAvailable**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein Update verfügbar ist.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**Pix \_ DXGI- \_ Status \_ keine \_ Umleitung**  
Ein benutzerdefiniertes HRESULT, für das der DXGI- \_ Status \_ keine \_ Umleitung hat.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**Pix \_ DXGI \_ \_ -Status ohne \_ Desktop \_ Zugriff**  
Ein benutzerdefiniertes HRESULT, das für den DXGI \_ \_ -Status keinen \_ Desktop \_ Zugriff hat.

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**Pix- \_ DXGI- \_ Status \_ Grafik \_ VidPN- \_ Quelle wird \_ \_ verwendet**  
Ein benutzerdefiniertes HRESULT, das von der in Verwendung von Echos DXGI- \_ Status \_ Grafik \_ VidPN \_ \_ \_ verwendet wird

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**Pix \_ DXGI- \_ Status \_ Modus \_ geändert**  
Ein benutzerdefiniertes HRESULT, für das der \_ Status Modus von " \_ \_ .

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ Status \_ Modus \_ \_ für \_ pix DXGI-Status wird geändert**  
Ein benutzerdefiniertes HRESULT, in dem der Status Modus für den DXGI- \_ Status \_ geändert wird \_ \_ \_ .

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**Pix \_ DXGI- \_ Status wurde \_ aufgehoben**  
Ein benutzerdefiniertes HRESULT, das den DXGI- \_ Status " \_ aufgehoben" hat.

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**Pix \_ DXGI- \_ Status- \_ DDA \_ wurde \_ immer noch \_ gezeichnet.**  
Ein benutzerdefiniertes HRESULT, das der DXGI- \_ Status- \_ DDA \_ \_ nach wie vor \_ zeichnet.

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**Pix \_ E \_ notimpl**  
Ein benutzerdefiniertes HRESULT, das von der Meldung E benachrichtigt wird \_ .

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**Pix \_ E \_ nointerface**  
Ein benutzerdefiniertes HRESULT, das auf " \_ nointerface" fest.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**Pix \_ E- \_ Zeiger**  
Ein benutzerdefiniertes HRESULT, das einen Zeiger auf einen \_ Zeiger hat

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**Pix \_ E \_ Abbrechen**  
Ein benutzerdefiniertes HRESULT, das den \_ Abbruch abbricht.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**Pix \_ E \_ schlägt fehl**  
Ein benutzerdefiniertes HRESULT, bei dem ein Fehler auftritt \_ .

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**Pix \_ E \_ unerwartet**  
Ein benutzerdefiniertes HRESULT, das von Echos E \_ unerwartet ist.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**Pix \_ E \_ AccessDenied**  
Ein benutzerdefiniertes HRESULT, auf das der Zugriff \_ verweigert wird.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**Pix- \_ E- \_ handle**  
Ein benutzerdefiniertes HRESULT, das mit dem-Wert von " \_

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**Pix \_ E \_ outo-Memory**  
Ein benutzerdefiniertes HRESULT, das auf den Wert von \_ outo-Memory zurückgeht

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**Pix \_ E \_ invalidArg**  
Ein benutzerdefiniertes HRESULT, das auf \_ invalidArg steht.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**Pix Xbox Fehler Datenträger \_ \_ \_ \_ voll**  
Ein benutzerdefiniertes HRESULT, das angibt, dass der Datenträger voll ist.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**Pix \_ WS \_ E \_ Adresse \_ in \_ Verwendung**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die Adresse bereits verwendet wird.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**Pix \_ WS \_ E \_ - \_ Richtlinie für fehlende Kits \_**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die Adresse nicht verfügbar ist.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**Pix \_ te \_ failedtoloadsoftwaremodule**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein erforderlicher Softwaremodul nicht geladen werden konnte.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**Pix \_ te \_ usedsoftwaremodulethatwasntwarporref**  
Ein benutzerdefiniertes HRESULT, das angibt, dass das verwendete Softwaremodul nicht der Warp-oder ref-Treiber war.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**Pix \_ te beschädigte \_ Datei**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die Datei beschädigt ist.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**Pix \_ te \_ faileddeopenfile**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die Datei nicht geöffnet werden konnte.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**Pix \_ te \_ callfailedonplayback**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein Fehler während der Wiedergabe aufgetreten ist

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**Pix \_ te \_ unknownuuid**  
Ein benutzerdefiniertes HRESULT, das angibt, dass eine unbekannte UUID gefunden wurde. Dies sollte nie vorkommen.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**Pix \_ te \_ notcapturefileorbeschädigte**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die Datei keine Erfassungs Datei ist oder beschädigt ist.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**Pix \_ te- \_ netzwerdatei**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**Pix \_ te \_ OlderFile**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**Pix \_ te \_ invalidmoment**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**Pix \_ - \_ Treiber "schlecht" \_**  
Ein benutzerdefiniertes HRESULT, das angibt, dass der Treiber schlecht ist.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**Pix \_ - \_ Fehler \_ \_ beim Zugriff auf depthstencil \_ in der \_ CPU.**  
Ein benutzerdefiniertes HRESULT, das angibt, dass die CPU versucht hat, auf den tiefen Schablonen Puffer zuzugreifen, was zu einem Fehler führt.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**Pix- \_ Fehler beim \_ Auflösen von \_ \_ Multisampling- \_ Textur.**  
Ein benutzerdefiniertes HRESULT, das angibt, dass versucht wurde, eine Multisampling-Textur aufzulösen, was zu einem Fehler führt.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**Pix \_ DXGI- \_ Fehler \_ ungültiger \_ Rückruf**  
Ein benutzerdefiniertes HRESULT, für das der Befehl "Echos DXGI" \_ \_ ungültig ist \_

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**Pix \_ DXGI- \_ Fehler \_ nicht \_ gefunden.**  
Ein benutzerdefiniertes HRESULT, das der DXGI- \_ Fehler \_ nicht \_ gefunden hat.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**Pix \_ DXGI- \_ Fehler \_ Weitere \_ Daten**  
Ein benutzerdefiniertes HRESULT, das für DXGI einen \_ Fehler \_ mehr \_ Daten verursacht.

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**Pix \_ DXGI- \_ Fehler \_ nicht unterstützt**  
Ein benutzerdefiniertes HRESULT, das den DXGI-Fehler "" \_ \_ nicht unterstützt

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**Pix- \_ DXGI- \_ Fehler \_ Gerät \_ entfernt**  
Ein benutzerdefiniertes HRESULT, das von der Meldung DXGI \_ Error \_ \_ entfernt wurde.

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**Pix \_ DXGI- \_ Fehler \_ Gerät \_ nicht reagiert**  
Ein benutzerdefiniertes HRESULT, das auf das-DXGI- \_ Fehler \_ Gerät reagiert \_ .

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**Pix \_ DXGI- \_ Fehler beim \_ \_ Zurücksetzen des Geräts**  
Ein benutzerdefiniertes HRESULT, das beim \_ \_ \_ Zurücksetzen von "DXGI"-Fehlern

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**Pix \_ DXGI- \_ Fehler \_ war \_ immer noch \_ gezeichnet.**  
Ein benutzerdefiniertes HRESULT, das den Fehler "Echos DXGI" \_ \_ \_ immer noch \_ zeichnet.

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**Pix \_ DXGI- \_ Fehler \_ Rahmen \_ Statistik \_ getrennt**  
Ein benutzerdefiniertes HRESULT, bei dem die Fehler in der DXGI- \_ Fehler \_ Frame \_ Statistik \_ getrennt werden

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**Pix \_ DXGI- \_ Fehler \_ Grafik \_ VidPN-Quelle wird \_ \_ \_ verwendet**  
Ein benutzerdefiniertes HRESULT, das bei der Verwendung von Echos DXGI \_ Error \_ Graphics \_ VidPN \_ Source \_ verwendet wird \_ .

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_Interner Fehler des pix DXGI- \_ Fehler \_ Treibers. \_ \_**  
Ein benutzerdefiniertes HRESULT, das einen internen Fehler des DXGI- \_ Fehler \_ Treibers verursacht \_ \_

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**Pix \_ DXGI- \_ Fehler \_ nicht exklusiv**  
Ein benutzerdefiniertes HRESULT, das für den DXGI- \_ Fehler \_ nicht exklusiv ist.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**Pix \_ DXGI- \_ Fehler ist \_ \_ zurzeit nicht \_ verfügbar.**  
Ein benutzerdefiniertes HRESULT, das für den Fehler "Echos DXGI" \_ \_ nicht \_ \_ verfügbar ist

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**Pix \_ DXGI- \_ Fehler " \_ Remote \_ Client \_ getrennt"**  
Ein benutzerdefiniertes HRESULT, für das der DXGI-Fehler für den \_ \_ Remote \_ Client \_ nicht

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**Pix \_ DXGI \_ - \_ Remote- \_ oudef-Fehler**  
Ein benutzerdefiniertes HRESULT, das auf einen remoten DXGI-Fehler zurückgeht \_ \_ \_ .

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**Pix- \_ DXGI- \_ fehlermodusänderung \_ \_ \_ in \_ Bearbeitung**  
Ein benutzerdefiniertes HRESULT, bei dem der Status der Echos DXGI- \_ Fehlermeldung \_ \_ geändert wird \_ \_ .

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**Pix \_ DXGI- \_ Fehler beim \_ Zugriff \_ verloren**  
Ein benutzerdefiniertes HRESULT, das für den Zugriff auf den DXGI- \_ Fehler in \_ \_

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**Pix \_ DXGI- \_ Fehler \_ Wartezeit- \_ Timeout**  
Ein benutzerdefiniertes HRESULT, das den Timeout Wert für DXGI- \_ Fehler \_ Wartezeiten \_

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**Pix \_ DXGI- \_ Fehler \_ Sitzung \_ getrennt**  
Ein benutzerdefiniertes HRESULT, für das die DXGI- \_ Fehler Sitzung von " \_ \_ .

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**Pix \_ DXGI \_ - \_ Fehler \_ auf \_ Ausgabe \_ veraltet beschränken**  
Ein benutzerdefiniertes HRESULT, das von "Echos DXGI \_ Error" \_ \_ auf \_ Ausgabe veraltet beschränkt wird \_ .

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**Pix \_ DXGI \_ - \_ Fehler \_ kann \_ Inhalte nicht schützen.**  
Ein benutzerdefiniertes HRESULT, das der DXGI-Fehler "Echos" \_ \_ nicht \_ schützen kann \_

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**Pix \_ DXGI- \_ Fehler \_ Zugriff \_ verweigert**  
Ein benutzerdefiniertes HRESULT, auf das der DXGI- \_ Fehler \_ Zugriff \_ verweigert wurde.

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**Pix \_ DXGI- \_ Fehler \_ Name ist \_ bereits \_ vorhanden.**  
Ein benutzerdefiniertes HRESULT, das den Namen "Echos DXGI \_ Error" \_ bereits enthält \_ \_ .

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**Pix- \_ DXGI- \_ Fehler-SDK- \_ \_ Komponente \_ fehlt**  
Ein benutzerdefiniertes HRESULT, das für die "DXGI \_ Error \_ SDK \_ Component" \_ fehlt.

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**Pix \_ DXGI \_ DDI \_ Err \_ wasstilldrawing**  
Ein benutzerdefiniertes HRESULT, das auf DXGI \_ DDI \_ Err \_ wasstilldrawing festgelegt ist.

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**Pix \_ DXGI \_ DDI \_ Err \_ wird nicht unterstützt.**  
Ein benutzerdefiniertes HRESULT, das von Echos DXGI \_ DDI \_ Err \_ nicht unterstützt wird.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**Pix \_ DXGI \_ DDI \_ Err \_ nicht exklusiv**  
Ein benutzerdefiniertes HRESULT, das auf "DXGI \_ DDI \_ Err nicht exklusiv" fest liegt \_ .

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**Pix \_ d3d10 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte**  
Ein benutzerdefiniertes HRESULT, das den \_ Fehler d3d10 \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte verursacht.

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**Pix \_ d3d10 \_ Fehler \_ Datei \_ nicht \_ gefunden.**  
Ein benutzerdefiniertes HRESULT, das die Fehler Datei "d3d10" \_ \_ \_ nicht \_ gefunden hat.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**Pix \_ D3D11 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte**  
Ein benutzerdefiniertes HRESULT, das den \_ Fehler D3D11 \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte verursacht.

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**Pix \_ D3D11 \_ Fehler \_ Datei \_ nicht \_ gefunden.**  
Ein benutzerdefiniertes HRESULT, das die Fehler Datei "D3D11" \_ \_ \_ nicht \_ gefunden hat.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**Pix \_ D3D11 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Ansichts \_ Objekte**  
Ein benutzerdefiniertes HRESULT, das den Fehler "D3D11" \_ \_ zu \_ viele \_ eindeutige \_ Ansichts \_ Objekte verursacht

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**Pix \_ D3D11 \_ Fehler bei \_ verzögerter \_ Kontext Zuordnung \_ \_ ohne \_ anfängliche \_ verwerfen**  
Ein benutzerdefiniertes HRESULT, das eine \_ Fehlermeldung zurückgibt \_ \_ \_ \_ \_ \_

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**Pix- \_ Fehler beim \_ \_ Zeichnen \_ -Befehl.**  
Ein benutzerdefiniertes HRESULT, das angibt, dass ein Draw-Befehl vollständig geokelt wurde, was zu einem Fehler führt.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



