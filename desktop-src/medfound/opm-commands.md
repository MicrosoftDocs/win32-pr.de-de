---
description: OPM-Befehle
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6d21119f86ab8f51392df248498681f8fe5dc1aa8218a0232b9f3bd1c7cb02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722240"
---
# <a name="opm-commands"></a>OPM-Befehle

In diesem Abschnitt werden die verfügbaren Befehle für [Output Protection Manager](output-protection-manager.md) (OPM) aufgelistet.

Um einen OPM-Befehl zu senden, rufen Sie [**IOPMVideoOutput::Configure auf.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) Für jeden Befehl werden die folgenden Informationen aufgeführt.



| Wert             | Beschreibung                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehls-GUID | Identifiziert den Befehl. Legen Sie den **guidSetting-Member** der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) auf diesen Wert fest. |
| Eingabedaten   | Gibt an, wie das **abParameters-Array** in der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) interpretiert werden soll.                      |



 

Die folgenden Befehle sind definiert:



| Get-Help                                                                                                       | Beschreibung                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING**](opm-set-acp-and-cgmsa-signaling.md)                               | Gibt andere Informationen zum Videosignal als die Schutzebene an.                      |
| [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Aktualisiert die Systemerneubarkeitsmeldung (System Renewability Message, SRM) für High-Bandwidth Digital Content Protection (HDCP). |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md)                                               | Legt die Schutzebene für einen Ausgabeschutzmechanismus fest.                                       |
| [**OPM \_ LEGT \_ \_ SCHUTZEBENE GEMÄß \_ \_ \_ \_ CSS-DVD FEST**](opm-set-protection-level-according-to-css-dvd.md) | Legt die HDCP-Schutzebene für die DVD-Wiedergabe gemäß den REGELN des DVD Content Scramble System (CSS) fest. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmierreferenz](opm-programming-reference.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 



