---
description: OPM-Statusanforderungen
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: OPM-Statusanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120175"
---
# <a name="opm-status-requests"></a>OPM-Statusanforderungen

In diesem Abschnitt werden die verfügbaren Statusanforderungen für [Output Protection Manager](output-protection-manager.md) (OPM) aufgeführt. Um eine OPM-Statusanforderung zu senden, rufen Sie [**IOPMVideoOutput::GetInformation auf.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) Für jede Anforderung werden die folgenden Informationen aufgeführt.



| Wert             | Beschreibung                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anforderungs-GUID | Identifiziert die Anforderung. Legen Sie **den guidSetting-Member** der [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) auf diesen Wert fest. |
| Eingabedaten   | Gibt an, wie das **abParameters-Array** in der [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur interpretiert**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) wird.                      |
| Ausgabedaten  | Gibt an, wie das **abRequestedInformation-Array** in der [**OPM \_ REQUESTED \_ INFORMATION-Struktur interpretiert**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) wird.         |



 

Die folgenden Statusanforderungen werden definiert:



| Statusanforderung                                                                                      | Beschreibung                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPM \_ GET ACP AND CGMSA SIGNALING (OPM GET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG) \_**](opm-get-acp-and-cgmsa-signaling.md)                     | Gibt die folgenden Informationen zu einer Videoausgabe zurück:                                                                                               |
| [**OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT**](opm-get-actual-output-format.md)                            | Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.                                                               |
| [**OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL**](opm-get-actual-protection-level.md)                      | Gibt die globale Schutzebene für einen angegebenen Schutzmechanismus zurück.                                                                             |
| [**OPM \_ GET \_ ADAPTER \_ BUS \_ TYPE**](opm-get-adapter-bus-type.md)                                    | Gibt den Typ des E/A-Bus zurück, der von der Videoausgabe verwendet wird.                                                                                                 |
| [**OPM \_ GET \_ CODEC \_ INFO**](opm-get-codec-info.md)                                                 | Ruft den Wert eines Hardwarecodecs ab.                                                                                                             |
| [**OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION**](opm-get-connected-hdcp-device-information.md) | Ruft Informationen zu einem High-Bandwidth Digital Content Protection (HDCP) ab, das an die Videoausgabe angefügt ist. Die folgenden Informationen werden zurückgegeben: |
| [**OPM \_ GET \_ CONNECTOR \_ TYPE**](opm-get-connector-type.md)                                         | Gibt den physischen Connectortyp der Videoausgabe zurück.                                                                                              |
| [**OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION**](opm-get-current-hdcp-srm-version.md)                   | Gibt die Versionsnummer der Systemerneuerbarkeitsmeldung (SRM) zurück, die derzeit von der Videoausgabe verwendet wird.                                               |
| [**OPM \_ GET \_ DVI \_ CHARACTERISTICS**](opm-get-dvi-characteristics.md)                               | Fragt ab, ob ein DVI-Connector (Digital Video Interface) DVI Version 1.1 oder höher unterstützt.                                                          |
| [**OPM \_ GET \_ OUTPUT \_ ID**](opm-get-output-id.md)                                                   | Gibt den eindeutigen Bezeichner des Monitors zurück, der dieser Videoausgabe zugeordnet ist.                                                                       |
| [**OPM \_ GET \_ SUPPORTED \_ PROTECTION \_ TYPES**](opm-get-supported-protection-types.md)                | Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.                                                                        |
| [**OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL**](opm-get-virtual-protection-level.md)                    | Gibt die virtuelle Schutzebene für einen angegebenen Schutzmechanismus zurück.                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[OPM-Programmierreferenz](opm-programming-reference.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 



