---
description: Die folgenden Strukturen werden mit dem Ausgabeschutz-Manager (Output Protection Manager, OPM) verwendet.
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: OPM-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35d72c5a5301dbc07b990aa4076f14fc221a1fde6af9c81e1f4a37fb424e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737647"
---
# <a name="opm-structures"></a>OPM-Strukturen

Die folgenden Strukturen werden mit [dem Ausgabeschutz-Manager (Output Protection Manager,](output-protection-manager.md) OPM) verwendet.



| Struktur                                                                                              | Beschreibung                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GRL-HEADER**](grl-header.md)                                                                      | Enthält den GRL-Header (Global Revocation List).                                                                                                          |
| [**MF \_ SIGNATURE**](mf-signature.md)                                                                  | Enthält eine GRL-Signatur (Global Revocation List).                                                                                                         |
| [**OPM \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Enthält das Ergebnis einer [**OPM \_ GET ACP AND \_ \_ \_ CGMSA \_ SIGNALING-Abfrage.**](opm-get-acp-and-cgmsa-signaling.md)                                         |
| [**\_TATSÄCHLICHES \_ \_ AUSGABEFORMAT VON OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Enthält das Ergebnis einer [**OPM \_ GET ACTUAL OUTPUT \_ \_ \_ FORMAT-Abfrage**](opm-get-actual-output-format.md) im Ausgabeschutz-Manager (OPM).               |
| [**OPM \_ CONFIGURE PARAMETERS (OPM-PARAMETER KONFIGURIEREN) \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Enthält einen OPM- oder Certified Output Protection Manager-Befehl (COPP).                                                                                     |
| [**INFORMATIONEN \_ ZUM VERBUNDENEN \_ HDCP-GERÄT \_ MIT OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Enthält das Ergebnis einer [**OPM \_ GET CONNECTED \_ \_ HDCP DEVICE \_ \_ INFORMATION-Abfrage.**](opm-get-connected-hdcp-device-information.md)                     |
| [**OPM \_ \_ COPP-KOMPATIBLE \_ GET \_ \_ INFO-PARAMETER**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Enthält Parameter für die [**IOPMVideoOutput::COPPCompatibleGetInformation-Methode.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) |
| [**OPM ENCRYPTED INITIALIZATION PARAMETERS (OPM \_ \_ ENCRYPTED-INITIALISIERUNGSPARAMETER) \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Enthält Initialisierungsparameter für eine OPM-Sitzung.                                                                                                     |
| [**ABRUFEN \_ VON \_ \_ CODEC-INFORMATIONEN \_ IN OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Enthält das Ergebnis einer [**OPM \_ GET CODEC \_ \_ INFO-Abfrage.**](opm-get-codec-info.md)                                                                     |
| [**OPM \_ GET \_ CODEC \_ INFO \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Enthält Informationen für den [**BEFEHL OPM \_ GET CODEC \_ \_ INFO.**](opm-get-codec-info.md)                                                                  |
| [**OPM GET INFO PARAMETERS (OPM \_ GET \_ \_ INFO-PARAMETER)**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Enthält Parameter für die [**IOPMVideoOutput::GetInformation-Methode.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)                             |
| [**OPM \_ HDCP \_ KEY \_ SELECTION \_ VECTOR**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Enthält den Schlüsselauswahlvektor (Key Selection Vector, KSV) für einen HDCP-Empfänger (High-Bandwidth Digital Content Protection).                                                   |
| [**OPM \_ OMAC**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Enthält eine Nachrichtenauthentifizierungscode (MAC) für eine OPM-Nachricht.                                                                                           |
| [**\_ \_ OPM-AUSGABE-ID-DATEN \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Enthält das Ergebnis einer [**OPM \_ GET OUTPUT \_ \_ ID-Statusanforderung.**](opm-get-output-id.md)                                                              |
| [**OPM \_ RANDOM \_ NUMBER**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Enthält eine 128-Bit-Zufallszahl für die Verwendung mit OPM.                                                                                                         |
| [**VON OPM \_ ANGEFORDERTE \_ INFORMATIONEN**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Enthält das Ergebnis einer OPM-Statusanforderung.                                                                                                              |
| [**OPM \_ SET ACP AND CGMSA SIGNALING PARAMETERS (OPM SET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNGSPARAMETER) \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Enthält Informationen zum [**OPM \_ SET ACP AND \_ \_ \_ CGMSA \_ SIGNALING-Befehl**](opm-set-acp-and-cgmsa-signaling.md) in OPM.                               |
| [**OPM \_ SET \_ HDCP SRM PARAMETERS (HDCP-SRM-PARAMETER FESTLEGEN) \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Enthält Parameter für den [**BEFEHL OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)                                                                       |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Enthält Daten für den [OPM \_ SET PROTECTION \_ \_ LEVEL-Befehl](opm-set-protection-level.md) in OPM.                                                          |
| [**OPM \_ \_ STANDARD-INFORMATIONEN**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Enthält das Ergebnis einer OPM-Statusanforderung.                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmierreferenz](opm-programming-reference.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 



