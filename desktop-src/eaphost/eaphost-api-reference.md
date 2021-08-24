---
title: EAPHost-API-Referenz
description: Erfahren Sie mehr über EAPHost-APIs und deren Komponenten. Referenzinformationen zu verschiedenen API-Themen, z. B. zum EAPHost-XML-Schema, finden Sie hier.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c522698999bcb58b4e33b8e1cb0d1bb74ae64fc3b709ce672b35e7db81e85ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739100"
---
# <a name="eaphost-api-reference"></a>EAPHost-API-Referenz

Die EAPHost-APIs sind in drei Komponenten unterteilt: die applizierten APIs, die direkt von einer EAP-fähigen Anwendung aufgerufen werden können. die EAP-Peermethoden-APIs, die Unterstützungsanforderungen für einen bestimmten EAP-Authentifizierungstyp verwalten und interaktive Elemente auf dem Client auslösen; und die EAP-Authentifikator-APIS, die die serverseitige Authentifizierung einer Unterstützung durchführen.

Die beiden letzten API-Komponenten – die EAP-Peermethode und die EAP-Authenticator-Methoden-APIs – erfordern eine benutzerdefinierte und konforme Implementierung in DLLs, die sie für den EAPHost-Dienst verfügbar machen. Sie können nicht direkt aus dem Anwendungscode aufgerufen werden. stattdessen werden sie von EAPHost aufgerufen (clientseitig für EAP-Peermethoden und auf der Serverseite für EAP-Authentifikatormethoden), wenn die Implementierung mit den API-Signaturen übereinstimmt, die in der entsprechenden Dokumentation angegeben sind. Spezifische Informationen zur API-Implementierung werden auf jeder Funktionsreferenzseite bereitgestellt.

## <a name="eaphost-registry-settings"></a>EAPHost Registry Einstellungen



| Thema                                                      | Beschreibung                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [EAPHost Registry Einstellungen](eaphost-registry-settings.md) | Beschreibt die registrierungsschlüssel, die von EAPHost verwendet werden. |



 

## <a name="eaphost-xml-schema"></a>EAPHost-XML-Schema



| Thema                                            | Beschreibung                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost und Legacyschema](eaphost-schemas.md) | Beschreibt das EAPHost-Schema und das Legacyschema zum Erstellen von XML-Konfigurations- und Anmeldeinformations-XML. |



 

## <a name="common-eaphost-api-reference"></a>Allgemeine Referenz zur EAPHost-API



| Thema                                                                   | Beschreibung                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Allgemeine EAPHost-API-Enumerationen](common-eap-host-api-enumerations.md) | Listet Konstanten auf, die allen EAPHost-APIs gemeinsam sind.  |
| [Allgemeine EAPHost-API-Strukturen](common-eap-host-api-structures.md)     | Listet Strukturen auf, die allen EAPHost-APIs gemeinsam sind. |
| [Allgemeine EAPHost-API-Konstanten](common-eap-host-error-constants.md)     | Listet Konstanten auf, die allen EAPHost-APIs gemeinsam sind.  |



 

## <a name="eaphost-api-reference"></a>EAPHost-API-Referenz



| Thema                                                                       | Beschreibung                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Referenz zur EAPHost-Supplipliplizierungs-API](eap-host-supplicant-api-reference.md)   | Beschreibt die API-Elemente, die verfügbar sind, um unterstützungsaufrufe an EAPHost zu aktivieren.                                                                      |
| [Api-Referenz zur EAPHost-Peermethode](eap-host-peer-method-api-reference.md) | Beschreibt die API-Elemente, die implementiert werden müssen, um eine EAP-Peermethoden-DLL zu erstellen, die von einem Client-EAPHost geladen und aufgerufen werden kann.          |
| [EAPHost Authenticator-Methoden-APIs](eaphost-authenticator-method-apis.md)  | Beschreibt die API-Elemente, die implementiert werden müssen, um eine EAP-Authentifikatormethoden-DLL zu erstellen, die von einem Server-EAPHost geladen und aufgerufen werden kann. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu EAPHost](about-eap-host.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> </dl>

 

 




