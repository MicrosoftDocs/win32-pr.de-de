---
title: EAPHost und Legacyschema
description: Beschreibt das EAPHost-Schema und das Legacyschema zum Erstellen von XML-Konfigurations- und Anmeldeinformations-XML.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4eb9f09a0f1380ad0373ec1171b0b0ea9101af87335d25287969d9a5f7f2da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984230"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost und Legacyschema

In diesem Thema werden das EAPHost-Schema und das Legacyschema zum Erstellen von XML-Konfigurations- und Anmeldeinformations-XML beschrieben.

## <a name="about-eaphost-and-legacy-schema"></a>Informationen zu EAPHost und Legacyschema

Das Erstellen von Konfigurations-XML beginnt mit dem [eaphostconfig-Schema.](eaphostconfigschema-schema.md) Das Erstellen von XML-Anmeldeinformationen beginnt mit dem [eaphostusercredentials-Schema.](eaphostusercredentialsschema-schema.md)

Einige der systemeigenen und älteren Schemas enthalten allgemeine Schemaelemente. Allgemeine Elemente, die in methodenkonfigurations- und methodenanmeldeinformationen verwendet werden, werden in einer einzelnen Schemadatei abstrahiert, die als "allgemeines Schema" bezeichnet wird.

Die Begriffe "Methodenkonfiguration" und "Verbindungseigenschaften" werden synonym verwendet. Ebenso werden die Begriffe "Methodenanmeldeinformationen" und "Benutzereigenschaften" synonym verwendet.

## <a name="eaphost-schema"></a>EAPHost-Schema



| Schema                                                                        | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Enthält allgemeine Konfigurationsschemaelemente.     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | Enthält allgemeine Schemaelemente für Anmeldeinformationen.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Enthält die **EapMethodType-Elementdefinition.** |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Enthält das EAPHost-Konfigurationsschema.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Enthält das EAPHost-Anmeldeinformationsschema.                |



 

## <a name="legacy-schema"></a>Legacyschema



| Schema                                                                            | BESCHREIBUNG                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Enthält allgemeine Konfigurationsschemaelemente.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Enthält allgemeine Schemaelemente für Anmeldeinformationen.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Enthält allgemeine Konfigurationsschemaelemente.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Enthält allgemeine Schemaelemente für Anmeldeinformationen.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Wird mit EAP-TLS verwendet, um Authentifizierungskonfigurationsdaten zu beschreiben.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Wird mit EAP-TLS verwendet, um Authentifizierungskonfigurationsdaten zu beschreiben, die mit Windows 7 beginnen. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Wird mit EAP-TLS verwendet, um Authentifizierungsanmeldeinformationen und Anmeldeinformationsoptionen zu beschreiben.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Wird mit MS-CHAPv2 verwendet, um Authentifizierungskonfigurationsdaten zu beschreiben.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Wird mit MS-CHAPv2 verwendet, um Anmeldeinformationen und Anmeldeinformationsoptionen für die Authentifizierung zu beschreiben.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Wird mit PEAPv0 verwendet, um Authentifizierungskonfigurationsdaten zu beschreiben.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Wird mit PEAPv0 verwendet, um Authentifizierungskonfigurationsdaten zu beschreiben, die mit Windows 7 beginnen.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Wird mit PEAPv0 verwendet, um Authentifizierungsanmeldeinformationen und Anmeldeinformationsoptionen zu beschreiben.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überprüfen von EAPHost- und Legacyschemabeispielen](eaphost-schemas.md)
</dt> </dl>

 

 




