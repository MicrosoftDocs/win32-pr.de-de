---
description: OPM-Befehle
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372918"
---
# <a name="opm-commands"></a>OPM-Befehle

In diesem Abschnitt werden die verfügbaren Befehle für den [Output Protection Manager](output-protection-manager.md) (OPM) aufgelistet.

Um einen OPM-Befehl zu senden, nennen Sie [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Die folgenden Informationen sind für jeden Befehl aufgeführt.



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehls-GUID | Identifiziert den-Befehl. Legen Sie den **guidsetting** -Member der [**OPM-Struktur \_ configure \_ Parameters**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) auf diesen Wert fest. |
| Eingabedaten   | Gibt an, wie das **abparameter** -Array in der OPM-Struktur " [**\_ configure \_ Parameters**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) " interpretiert wird.                      |



 

Die folgenden Befehle sind definiert:



| Get-Help                                                                                                       | BESCHREIBUNG                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung**](opm-set-acp-and-cgmsa-signaling.md)                               | Gibt Informationen über das Videosignal außer der Schutz Ebene an.                      |
| [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Aktualisiert die System-erneuerbarkeits Meldung (SRM) für High-Bandwidth Digital Content Protection (HDCP). |
| [**OPM \_ - \_ Schutz \_ Ebene festlegen**](opm-set-protection-level.md)                                               | Legt die Schutz Ebene für einen ausgabeschutzmechanismus fest.                                       |
| [**OPM \_ Festlegen der \_ Schutz \_ Ebene \_ gemäß CSS- \_ \_ \_ DVD**](opm-set-protection-level-according-to-css-dvd.md) | Legt die HDCP-Schutz Ebene für die DVD-Wiedergabe fest, und zwar gemäß den DVD-Inhalts Regeln für das Scramble-System |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmier Referenz](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



