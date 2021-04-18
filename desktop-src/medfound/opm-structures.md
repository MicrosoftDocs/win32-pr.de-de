---
description: Die folgenden Strukturen werden mit dem Output Protection Manager (OPM) verwendet.
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: OPM-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bc7cbc13b987a2cfdda5d210cddd2fd05b8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345814"
---
# <a name="opm-structures"></a>OPM-Strukturen

Die folgenden Strukturen werden mit dem [Output Protection Manager](output-protection-manager.md) (OPM) verwendet.



| Struktur                                                                                              | BESCHREIBUNG                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GRL- \_ Header**](grl-header.md)                                                                      | Enthält den GRL-Header (Global Sperrlist).                                                                                                          |
| [**MF- \_ Signatur**](mf-signature.md)                                                                  | Enthält eine GRL-Signatur (Global Sperrlist).                                                                                                         |
| [**OPM \_ -ACP \_ und \_ cgmsa- \_ Signalisierung**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Enthält das Ergebnis einer [**OPM \_ get \_ ACP- \_ und \_ cgmsa- \_ Signalisierungs**](opm-get-acp-and-cgmsa-signaling.md) Abfrage.                                         |
| [**tatsächliches OPM- \_ \_ Ausgabe \_ Format**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Enthält das Ergebnis einer Abfrage zum Abfragen des [**\_ \_ tatsächlichen \_ Ausgabe \_ Formats**](opm-get-actual-output-format.md) in Output Protection Manager (OPM).               |
| [**OPM- \_ Konfigurations \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Enthält einen OPM-oder Certified Output Protection Manager (COPP)-Befehl.                                                                                     |
| [**mit OPM \_ verbundene \_ HDCP- \_ Geräte \_ Informationen**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Enthält das Ergebnis einer [**OPM \_ get \_ Connected \_ HDCP \_ Device \_ Information**](opm-get-connected-hdcp-device-information.md) Query.                     |
| [**OPM \_ COPP- \_ kompatible \_ Get Info- \_ \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Enthält Parameter für die [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) -Methode. |
| [**verschlüsselte OPM- \_ \_ Initialisierungs \_ Parameter**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Enthält Initialisierungs Parameter für eine OPM-Sitzung.                                                                                                     |
| [**OPM \_ get \_ Codec \_ - \_ Informations Informationen**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Enthält das Ergebnis einer [**OPM \_ get \_ Codec \_ Info**](opm-get-codec-info.md) -Abfrage.                                                                     |
| [**OPM \_ get \_ Codec- \_ Informations \_ Parameter**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Enthält Informationen für den [**OPM-Befehl \_ get \_ Codec \_ Info**](opm-get-codec-info.md) .                                                                  |
| [**OPM \_ get \_ Info- \_ Parameter**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Enthält Parameter für die [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode.                             |
| [**OPM- \_ HDCP- \_ Schlüssel \_ Auswahl \_ Vektor**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Enthält den Schlüsselauswahl Vektor (KSV) für einen HDCP-Empfänger (High-Bandwidth Digital Content Protection).                                                   |
| [**OPM \_ OMAC**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Enthält einen Nachrichtenauthentifizierungscode (Mac) für eine OPM-Nachricht.                                                                                           |
| [**OPM- \_ Ausgabe- \_ ID- \_ Daten**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Enthält das Ergebnis einer [**OPM- \_ \_ Ausgabe- \_ ID**](opm-get-output-id.md) -Status Anforderung.                                                              |
| [**OPM- \_ Zufalls \_ Zahl**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Enthält eine Zufallszahl mit 128 Bit für die Verwendung mit OPM.                                                                                                         |
| [**von OPM \_ angeforderte \_ Informationen**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Enthält das Ergebnis einer OPM-Status Anforderung.                                                                                                              |
| [**OPM \_ -Festlegen von \_ ACP- \_ und \_ cgmsa- \_ Signalisierungs \_ Parametern**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Enthält Informationen für den [**OPM \_ \_ -Satz ACP- \_ und \_ cgmsa- \_ Signalisierungs**](opm-set-acp-and-cgmsa-signaling.md) Befehl in OPM.                               |
| [**OPM \_ Set \_ HDCP \_ SRM- \_ Parameter**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Enthält Parameter für den [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) -Befehl.                                                                       |
| [**OPM- \_ Parameter zum Festlegen der \_ Schutz \_ Ebene \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Enthält Daten für den [OPM-Befehl zum \_ Festlegen der \_ Schutz \_ Ebene](opm-set-protection-level.md) in OPM.                                                          |
| [**OPM- \_ Standard \_ Informationen**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Enthält das Ergebnis einer OPM-Status Anforderung.                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmier Referenz](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



