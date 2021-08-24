---
title: WMDM-Strukturen
description: Dieser Artikel enthält Referenzartikel zu Strukturen, die von Windows Media Geräte-Manager definiert werden, z. B. _BITMAPINFOHEADER und MTP_COMMAND_DATA_IN.
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Medien Geräte-Manager,Strukturen
- Geräte-Manager,Strukturen
- Programmierreferenz,Strukturen
- Referenz für Windows Media Geräte-Manager,structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd0048a7cf3b87f09bb46ef6f6db74531b4b67a7364acd28099feed04bb8dec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865540"
---
# <a name="wmdm-structures"></a>WMDM-Strukturen

Windows Media Geräte-Manager definiert die folgenden Strukturen.



| Struktur                                                   | BESCHREIBUNG                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Definiert das Format des Videoframes.                                                                                                                                                                                                                       |
| [**\_MTP-BEFEHLSDATEN \_ \_ IN**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Enthält benutzerdefinierte MTP-Befehle (Media Transport Protocol), die mithilfe der [**IWMDMDevice3::D eviceIoControl-Methode**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) an das Gerät gesendet werden.                                                                           |
| [**MTP \_ COMMAND \_ DATA \_ OUT**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Enthält MTP-Antworten (Media Transport Protocol), die vom Gerätetreiber ausgefüllt werden.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Enthält Daten für Befehle, die über Windows Media Geräte-Manager an ein Gerät übergeben werden, aber nicht von Windows Media Geräte-Manager verarbeitet werden sollen.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Definiert das Format eines Videostreams.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Definiert das Format von Waveform-Audiodaten.                                                                                                                                                                                                               |
| [**\_WMDM-FORMATFUNKTION \_**](wmdm-format-capability.md)  | Beschreibt die Funktionen eines Geräts für ein bestimmtes Format. Diese Struktur enthält einen Satz von Eigenschaftenkonfigurationen in einem Array von [**WMDM \_ PROP \_ CONFIG-Strukturen.**](wmdm-prop-config.md)                                                       |
| [**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)              | Beschreibt einen Satz kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschaftenbeschreibungen in einem Array von [**WMDM \_ PROP \_ DESC-Strukturen.**](wmdm-prop-desc.md) |
| [**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)                  | Beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.                                                                                                                                                                             |
| [**WMDM \_ PROP \_ VALUES \_ ENUM**](wmdm-prop-values-enum.md)   | Enthält einen Aufzählungssatz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.                                                                                                                                             |
| [**\_ \_ WMDM-PROP-WERTEBEREICH \_**](wmdm-prop-values-range.md) | Beschreibt den Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaftenkonfiguration.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Enthält ein Datum und eine Uhrzeit.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Beschreibt Seriennummern und Gruppen-IDs.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Definiert die Metadatenansicht.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Beschreibt Rechte zur Inhaltsverwendung.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Beschreibt einen MIME-Typ.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 




