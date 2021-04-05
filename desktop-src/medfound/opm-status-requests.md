---
description: OPM-Status Anforderungen
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: OPM-Status Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753913"
---
# <a name="opm-status-requests"></a>OPM-Status Anforderungen

In diesem Abschnitt werden die verfügbaren Status Anforderungen für den [Output Protection Manager](output-protection-manager.md) (OPM) aufgelistet. Um eine OPM-Status Anforderung zu senden, nennen Sie [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Für jede Anforderung werden die folgenden Informationen aufgelistet.



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | Gibt die Anforderung an. Legen Sie den **guidsetting** -Member der [**OPM-Struktur \_ get \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) auf diesen Wert fest. |
| Eingabedaten   | Gibt an, wie das **abparameter** -Array in der [**OPM-Struktur \_ get \_ Info \_ Parameters interpretiert werden**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) soll.                      |
| Ausgabedaten  | Gibt an, wie das **abrequestedinformation** -Array in der von [**OPM \_ angeforderten \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur interpretiert werden soll.         |



 

Die folgenden Status Anforderungen sind definiert:



| Status Anforderung                                                                                      | BESCHREIBUNG                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung**](opm-get-acp-and-cgmsa-signaling.md)                     | Gibt die folgenden Informationen zu einer Videoausgabe zurück:                                                                                               |
| [**OPM \_ get \_ tatsächliches \_ Ausgabe \_ Format**](opm-get-actual-output-format.md)                            | Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.                                                               |
| [**OPM \_ get \_ Actual \_ Protection \_ Level**](opm-get-actual-protection-level.md)                      | Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.                                                                             |
| [**OPM \_ get \_ Adapter \_ \_ Bustyp**](opm-get-adapter-bus-type.md)                                    | Gibt den Typ des e/a-Busses zurück, der von der Videoausgabe verwendet wird.                                                                                                 |
| [**OPM- \_ get- \_ Codec- \_ Informationen**](opm-get-codec-info.md)                                                 | Ruft den Verdienst Wert eines Hardware Codecs ab.                                                                                                             |
| [**OPM \_ get \_ Connected \_ HDCP- \_ Geräte \_ Informationen**](opm-get-connected-hdcp-device-information.md) | Ruft Informationen zu einem HDCP-Gerät (High-Bandwidth Digital Content Protection) ab, das an die Videoausgabe angehängt ist. Die folgenden Informationen werden zurückgegeben: |
| [**OPM \_ get \_ Connector- \_ Typ**](opm-get-connector-type.md)                                         | Gibt den physischen Verbindungstyp der Videoausgabe zurück.                                                                                              |
| [**OPM \_ get \_ Current \_ HDCP \_ SRM- \_ Version**](opm-get-current-hdcp-srm-version.md)                   | Gibt die Versionsnummer der von der Videoausgabe verwendeten SRM (System erneuerbarkeits Meldung) zurück.                                               |
| [**OPM- \_ get- \_ DVI- \_ Merkmale**](opm-get-dvi-characteristics.md)                               | Fragt ab, ob ein DVI-Connector (Digital Video Interface) die DVI-Version 1,1 oder höher unterstützt.                                                          |
| [**OPM \_ - \_ Ausgabe- \_ ID erhalten**](opm-get-output-id.md)                                                   | Gibt den eindeutigen Bezeichner des Monitors zurück, der mit dieser Videoausgabe verknüpft ist.                                                                       |
| [**OPM \_ - \_ unterstützte \_ Schutz \_ Typen erhalten**](opm-get-supported-protection-types.md)                | Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.                                                                        |
| [**OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_**](opm-get-virtual-protection-level.md)                    | Gibt die virtuelle Schutz Ebene für einen angegebenen Schutzmechanismus zurück.                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmier Referenz](opm-programming-reference.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



