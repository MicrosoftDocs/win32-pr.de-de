---
title: Remotedesktopprotokoll Anbieterstrukturen
description: Die benutzerdefinierte Remoteprotokoll-API unterstützt die folgenden Strukturen.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f7d1b7b3ea968925cdcace605ed6c136054b023cc12482475196696bdbcc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856236"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Remotedesktopprotokoll Anbieterstrukturen

Die benutzerdefinierte Remoteprotokoll-API unterstützt die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**\_TSMF-SUPPORTDATEN \_ \_ IN**](tsmf-support-data-in.md)
</dt> <dd>

Enthält Informationen zu Medienformaten.

</dd> <dt>

[**TSMF \_ SUPPORT \_ DATA \_ OUT**](tsmf-support-data-out.md)
</dt> <dd>

Enthält Informationen zu Medienformaten.

</dd> <dt>

[**\_TSMF-UNTERSTÜTZUNG \_ FÜR NODEDATA \_ IN**](tsmf-support-nodedata-in.md)
</dt> <dd>

Wird in der [**TSMF \_ SUPPORT \_ DATA \_ IN-Struktur**](tsmf-support-data-in.md) verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.

</dd> <dt>

[**TSMF \_ SUPPORT \_ NODEDATA \_ OUT**](tsmf-support-nodedata-out.md)
</dt> <dd>

Wird in der [**TSMF \_ SUPPORT \_ DATA \_ OUT-Struktur**](tsmf-support-data-out.md) verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.

</dd> <dt>

[**\_WRDS-VERBINDUNGSEINSTELLUNGEN \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Enthält Verbindungseinstellungsinformationen für eine Remotesitzung.

</dd> <dt>

[**\_WRDS-VERBINDUNGSEINSTELLUNGEN \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Enthält Verbindungseinstellungsinformationen für eine Remotesitzung.

</dd> <dt>

[**WRDS \_ – DYNAMISCHE \_ \_ \_ ZEITZONENINFORMATIONEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Enthält dynamische Zeitzoneninformationen.

</dd> <dt>

[**\_WRDS-LISTENEREINSTELLUNGEN \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Enthält Listenereinstellungsinformationen für eine Remotesitzung.

</dd> <dt>

[**WRDS \_ LISTENER \_ SETTINGS \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Enthält Listenereinstellungen für eine Remotesitzung.

</dd> <dt>

[**\_WRDS-EINSTELLUNGEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Enthält richtlinienbezogene Einstellungsinformationen für eine Remotesitzung.

</dd> <dt>

[**\_WRDS-EINSTELLUNGEN \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Enthält richtlinienbezogene Einstellungen für eine Remotesitzung.

</dd> <dt>

[**\_WTS CACHE \_ STATS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Enthält Protokollcachestatistiken.

</dd> <dt>

[**\_WTS ANZEIGEN \_ VON IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Enthält Informationen zur Clientanzeige.

</dd> <dt>

[**\_WTS \_CLIENTDATEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Enthält Informationen zur Clientverbindung.

</dd> <dt>

[**\_WTS \_LIZENZFUNKTIONEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Enthält Informationen zu den Lizenzierungsfunktionen des Clients.

</dd> <dt>

[**\_WTS \_RICHTLINIENDATEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Enthält Richtlinieninformationen, die vom Remotedesktopdienste-Dienst an das Protokoll übergeben werden.

</dd> <dt>

[**\_WTS PROPERTY \_ VALUE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Enthält Informationen zu einem Eigenschaftswert, der aus dem Protokoll abgerufen werden soll.

</dd> <dt>

[**\_WTS \_PROTOKOLLCACHE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Enthält die Anzahl der Cachelese- und Cachetreffer.

</dd> <dt>

[**\_WTS \_PROTOKOLLZÄHLER**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Enthält Protokollleistungsindikatoren.

</dd> <dt>

[**\_WTS \_PROTOKOLLSTATUS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Enthält Informationen zum Status des Protokolls.

</dd> <dt>

[**\_WTS \_DIENSTSTATUS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Enthält Informationen zu Änderungen im Status des Remotedesktopdienste-Diensts.

</dd> <dt>

[**\_WTS \_SITZUNGS-ID**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Enthält eine **GUID,** die eine Sitzung eindeutig identifiziert.

</dd> <dt>

[**\_WTS SMALL \_ RECT**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Enthält Clientfensterkoordinaten.

</dd> <dt>

[**\_WTS SOCKADDR**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Enthält eine Socketadresse.

</dd> <dt>

[**\_WTS Systemtime**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Gibt Datums- und Uhrzeitinformationen für Übergänge zwischen Normalzeit und Sommerzeit an.

</dd> <dt>

[**\_WTS \_ \_ ZEITZONENINFORMATIONEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Enthält Clientzeitzoneninformationen.

</dd> <dt>

[**\_WTS \_BENUTZERANMELDEINFORMATIONEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Enthält Anmeldeinformationen für einen Benutzer.

</dd> <dt>

[**\_WTS \_BENUTZERDATEN**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Enthält ausgewählte Clienteigenschaftswerte.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopprotokoll Anbieterreferenz](custom-remote-protocol-reference.md)
</dt> <dt>

[Remotedesktopprotokoll-Anbieterenumerationen](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Remotedesktopprotokoll-Anbieterschnittstellen](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Remotedesktopprotokoll Provider Unions](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




