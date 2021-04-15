---
title: EAPHost-API-Referenz
description: Erfahren Sie mehr über EAPHost-APIs und deren Komponenten. Siehe Referenzinformationen zu verschiedenen API-Themen, wie z. b. das XML-Schema von EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104390999"
---
# <a name="eaphost-api-reference"></a>EAPHost-API-Referenz

Die EAPHost-APIs sind in drei Komponenten unterteilt: die Supplicant-APIs, die direkt von einer EAP-fähigen Anwendung aufgerufen werden können. die APIs der EAP-Peer Methode, die Supplicant-Anforderungen für einen bestimmten EAP-Authentifizierungstyp verwalten und interaktive Elemente auf dem Client aufrufen. und die EAP Authenticator-APIs, die die serverseitige Authentifizierung eines Supplicant ausführen.

Die beiden letzten API-Komponenten (die EAP-Peer Methode und die EAP Authenticator-Methoden-APIs) erfordern eine benutzerdefinierte und konforme Implementierung in DLLs, die Sie für den EAPHost-Dienst verfügbar machen. Sie können nicht direkt aus dem Anwendungscode aufgerufen werden. Stattdessen werden Sie von EAPHost (auf Clientseite für EAP-Peer Methoden und auf der Serverseite für EAP Authenticator-Methoden) aufgerufen, wenn die Implementierung den in der entsprechenden Dokumentation angegebenen API-Signaturen entspricht. Spezifische Informationen zur API-Implementierung werden auf jeder Funktionsreferenz Seite bereitgestellt.

## <a name="eaphost-registry-settings"></a>EAPHost-Registrierungs Einstellungen



| Thema                                                      | BESCHREIBUNG                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md) | Beschreibt die von EAPHost genutzten Registrierungsschlüssel. |



 

## <a name="eaphost-xml-schema"></a>EAPHost-XML-Schema



| Thema                                            | BESCHREIBUNG                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost und Legacy Schema](eaphost-schemas.md) | Beschreibt das EAPHost-Schema und das Legacy Schema zum Erstellen von XML-Konfigurationsdateien und Anmelde Informationen. |



 

## <a name="common-eaphost-api-reference"></a>Allgemeine EAPHost-API-Referenz



| Thema                                                                   | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Allgemeine EAPHost-API-Enumerationen](common-eap-host-api-enumerations.md) | Listet Konstanten auf, die allen EAPHost-APIs gemeinsam sind.  |
| [Allgemeine EAPHost-API-Strukturen](common-eap-host-api-structures.md)     | Listet Strukturen auf, die allen EAPHost-APIs gemeinsam sind. |
| [Allgemeine EAPHost-API-Konstanten](common-eap-host-error-constants.md)     | Listet Konstanten auf, die allen EAPHost-APIs gemeinsam sind.  |



 

## <a name="eaphost-api-reference"></a>EAPHost-API-Referenz



| Thema                                                                       | BESCHREIBUNG                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [EAPHost-Supplicant-API-Referenz](eap-host-supplicant-api-reference.md)   | Beschreibt die verfügbaren API-Elemente, um Supplicant Aufrufe von EAPHost zu aktivieren.                                                                      |
| [API-Referenz für die EAPHost-Peer Methode](eap-host-peer-method-api-reference.md) | Beschreibt die API-Elemente, die implementiert werden müssen, um eine EAP-Peer Methoden-dll zu erstellen, die von einem Client-EAPHost geladen und aufgerufen werden kann.          |
| [EAPHost-Authenticator-Methoden-APIs](eaphost-authenticator-method-apis.md)  | Beschreibt die API-Elemente, die implementiert werden müssen, um eine EAP Authenticator-Methoden-dll zu erstellen, die von einem Server EAPHost geladen und aufgerufen werden kann. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu EAPHost](about-eap-host.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> </dl>

 

 




