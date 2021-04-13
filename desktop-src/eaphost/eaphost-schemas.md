---
title: EAPHost und Legacy Schema
description: Beschreibt das EAPHost-Schema und das Legacy Schema zum Erstellen von XML-Konfigurationsdateien und Anmelde Informationen.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389640"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost und Legacy Schema

In diesem Thema werden das EAPHost-Schema und das Legacy Schema zum Erstellen von XML-Konfigurationsdateien und Anmelde Informationsdateien beschrieben.

## <a name="about-eaphost-and-legacy-schema"></a>Informationen zu EAPHost und Legacy Schema

Das Erstellen einer Konfigurations-XML-Datei beginnt mit dem [eaphostconfig](eaphostconfigschema-schema.md) -Schema. das Erstellen von Anmelde Informations-XML-Daten beginnt mit dem [eaphustusercredeneschema](eaphostusercredentialsschema-schema.md) .

Einige der systemeigenen und Legacy Schemas enthalten allgemeine Schema Elemente. Allgemeine Elemente, die in Methoden Konfiguration und Methoden Anmelde Informationen verwendet werden, werden in eine einzelne Schema Datei abstrahiert, die als "Common Schema" bezeichnet wird.

Die Begriffe "Methoden Konfiguration" und "Verbindungs Eigenschaften" werden austauschbar verwendet. Ebenso werden die Begriffe "Methoden Anmelde Informationen" und "Benutzereigenschaften" austauschbar verwendet.

## <a name="eaphost-schema"></a>EAPHost-Schema



| Schema                                                                        | BESCHREIBUNG                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Enthält allgemeine Konfigurations Schema Elemente.     |
| [baseeapmethoduseranmeldeinformationen](baseeapmethodusercredentialsschema-schema.md) | Enthält allgemeine Schema Elemente für Anmelde Informationen.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Enthält die **eapmethodtype** -Element Definition. |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Enthält das EAPHost-Konfigurations Schema.             |
| [eaphustuseranmeldeinformationen](eaphostusercredentialsschema-schema.md)             | Enthält das EAPHost-Anmelde Informations Schema.                |



 

## <a name="legacy-schema"></a>Legacy Schema



| Schema                                                                            | BESCHREIBUNG                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Enthält allgemeine Konfigurations Schema Elemente.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Enthält allgemeine Schema Elemente für Anmelde Informationen.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Enthält allgemeine Konfigurations Schema Elemente.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Enthält allgemeine Schema Elemente für Anmelde Informationen.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Wird mit EAP-TLS verwendet, um die Konfigurationsdaten für die Authentifizierung zu beschreiben.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Wird mit EAP-TLS verwendet, um die Konfigurationsdaten für die Authentifizierung ab Windows 7 zu beschreiben. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Wird mit EAP-TLS verwendet, um Authentifizierungs Anmelde Informationen und Anmelde Informations Optionen zu beschreiben.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Wird mit MS-CHAPv2 verwendet, um die Authentifizierungs Konfigurationsdaten zu beschreiben.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Wird mit MS-CHAPv2 verwendet, um Authentifizierungs Anmelde Informationen und Anmelde Informations Optionen zu beschreiben.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Wird mit PEAPv0 verwendet, um die Konfigurationsdaten für die Authentifizierung zu beschreiben.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Wird mit PEAPv0 verwendet, um die Konfigurationsdaten für die Authentifizierung ab Windows 7 zu beschreiben.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Wird mit PEAPv0 verwendet, um Authentifizierungs Anmelde Informationen und Anmelde Informations Optionen zu beschreiben.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überprüfen von EAPHost-und Legacy-Schema Beispielen](eaphost-schemas.md)
</dt> </dl>

 

 




