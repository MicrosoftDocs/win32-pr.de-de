---
description: OPM-Befehle
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119145"
---
# <a name="opm-commands"></a>OPM-Befehle

In diesem Abschnitt werden die verfügbaren Befehle für [Output Protection Manager](output-protection-manager.md) (OPM) aufgeführt.

Um einen OPM-Befehl zu senden, rufen Sie [**IOPMVideoOutput::Configure auf.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) Für jeden Befehl werden die folgenden Informationen aufgeführt.



| Wert             | Beschreibung                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehls-GUID | Identifiziert den Befehl. Legen Sie **den guidSetting-Member** der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) auf diesen Wert fest. |
| Eingabedaten   | Gibt an, wie das **abParameters-Array** in der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur interpretiert**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) wird.                      |



 

Die folgenden Befehle sind definiert:



| Befehl                                                                                                       | Beschreibung                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ SET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG \_**](opm-set-acp-and-cgmsa-signaling.md)                               | Gibt Informationen über das Videosignal an, die nicht die Schutzebene sind.                      |
| [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Aktualisiert die Systemerneuerbarkeitsmeldung (SRM) für High-Bandwidth Digital Content Protection (HDCP). |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md)                                               | Legt die Schutzebene für einen Ausgabeschutzmechanismus fest.                                       |
| [**\_OPM: \_ FESTLEGEN DER \_ \_ SCHUTZEBENE GEMÄß \_ \_ \_ CSS-DVD**](opm-set-protection-level-according-to-css-dvd.md) | Legt die HDCP-Schutzebene für die DVD-Wiedergabe fest, die den CSS-Regeln (DVD Content Scramble System) folgt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmierreferenz](opm-programming-reference.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 



