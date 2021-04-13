---
title: WMDM-Strukturen
description: Strukturen
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Media-Device Manager, Strukturen
- Device Manager, Strukturen
- Programmier Referenz, Strukturen
- Referenz für Windows Media-Device Manager, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903aa07bbe3d01029eb2020b521523b545843f2a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389624"
---
# <a name="wmdm-structures"></a>WMDM-Strukturen

In Windows Media Device Manager werden die folgenden Strukturen definiert.



| Struktur                                                   | BESCHREIBUNG                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Definiert das Format des Video Frames.                                                                                                                                                                                                                       |
| [**MTP- \_ Befehls \_ Daten \_ in**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Enthält benutzerdefinierte MTP (Media Transport Protocol)-Befehle, die mithilfe der [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) -Methode an das Gerät gesendet werden.                                                                           |
| [**MTP- \_ Befehls \_ Datenausgabe \_**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Enthält MTP-Antworten (Media Transport Protocol), die vom Gerätetreiber ausgefüllt werden.                                                                                                                                                                  |
| [**Opaquecommand**](opaquecommand.md)                      | Enthält Daten für Befehle, die über Windows Media Device Manager an ein Gerät übermittelt werden, jedoch nicht von Windows Media Device Manager behandelt werden sollen.                                                                                       |
| [**\_Videoinfoheader**](-videoinfoheader.md)               | Definiert das Format eines Videodaten Stroms.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Definiert das Format von Waveform-Audiodaten.                                                                                                                                                                                                               |
| [**WMDM- \_ Format \_ Funktion**](wmdm-format-capability.md)  | Beschreibt die Funktionen eines Geräts für ein bestimmtes Format. Diese Struktur enthält eine Reihe von Eigenschaften Konfigurationen in einem Array von [**WMDM- \_ Prop- \_ Konfigurations**](wmdm-prop-config.md) Strukturen.                                                       |
| [**WMDM- \_ Prop- \_ Konfiguration**](wmdm-prop-config.md)              | Beschreibt einen Satz kompatibler Eigenschaftswerte für alle Eigenschaften, die vom Gerät für ein bestimmtes Format unterstützt werden. Diese Struktur enthält eine Reihe von Eigenschafts Beschreibungen in einem Array von [**WMDM-unter \_ \_**](wmdm-prop-desc.md) geordneten Strukturen. |
| [**WMDM- \_ Prop- \_ Abteilung**](wmdm-prop-desc.md)                  | Beschreibt gültige Werte einer Eigenschaft in einer bestimmten Eigenschaften Konfiguration.                                                                                                                                                                             |
| [**WMDM- \_ Prop \_ Values- \_ Enumeration**](wmdm-prop-values-enum.md)   | Enthält einen Aufzählungs Satz gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.                                                                                                                                             |
| [**Bereich der WMDM- \_ Prop- \_ Werte \_**](wmdm-prop-values-range.md) | Beschreibt den Bereich gültiger Werte für eine bestimmte Eigenschaft in einer bestimmten Eigenschaften Konfiguration.                                                                                                                                                        |
| [**Wmdmdatetime**](wmdmdatetime.md)                        | Enthält ein Datum und eine Uhrzeit.                                                                                                                                                                                                                                |
| [**Wmdmid**](wmdmid.md)                                    | Beschreibt Seriennummern und Gruppen-IDs.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Definiert die Metadatenansicht.                                                                                                                                                                                                                               |
| [**Wmdmrights**](wmdmrights.md)                            | Beschreibt Inhalts Nutzungsrechte.                                                                                                                                                                                                                            |
| [**Wmfilefunktionen**](wmfilecapabilities.md)            | Beschreibt einen MIME-Typ.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 




