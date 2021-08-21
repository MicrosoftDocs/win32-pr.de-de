---
title: SSO EAPHost Scenario Overview
description: Enthält zwei Szenarien, die die Vorteile einer SSO-fähigen Supplikation (Single Sign-On, einmaliges Anmelden) veranschaulichen.
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc9be7af26844004073f21154df5ac12cb44d4eaa04fddc457b729ffe5e1083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042778"
---
# <a name="sso-eaphost-scenario-overview"></a>SSO EAPHost Scenario Overview

Das folgende Thema enthält zwei Szenarien, die die Vorteile einer SSO-fähigen Unterstützung (Single Sign-On, SSO) veranschaulichen.

## <a name="about-the-scenarios"></a>Informationen zu den Szenarien

SSO bietet Funktionen zum Beibehalten zusätzlicher Benutzeranmeldeinformationen, die üblicherweise im EAP-Benutzerblob gespeichert werden. Im Gegensatz zu anderen Anmeldeinformationsprozessen können SSO-fähige Unterstützungsvorgänge Anmeldesituationen wie AP-Roaming und Kennwortänderungen ohne Benutzereingriff auflösen.

## <a name="sso-eap-tls-pin-caching-behavior"></a>SSO-EAP-TLS-PIN-Zwischenspeicherungsverhalten

Eine Unterstützung kann die Netzwerkauthentifizierung mithilfe einer Smartcard-basierten EAP-Methode wie Extensible Authentication Protocol Transport Layer Security (EAP-TLS) versuchen. In diesem und ähnlichen Szenarios ruft die Unterstützung die Smartcard-PIN vom Benutzer ab und ruft ein Benutzerzertifikat für die Netzwerkauthentifizierung ab, gefolgt von einem Aufruf von WinLogin auf dem lokalen Computer. Nach erfolgreicher Authentifizierung speichert die Unterstützung das Benutzer-BLOB zwischen und speichert keine Benutzer-PIN-Informationen.

Wenn der Benutzer zu einem anderen Speicherort übergibt, muss die Sitzungsaufbeendigung und die erneute Authentifizierung erfolgen. Da das Zertifikat nicht vor der Anmeldung gespeichert werden kann, schlägt die Benutzerauthentifizierung fehl, und die Unterstützung leert das Benutzerblob. An diesem Punkt ist die Benutzer-PIN erforderlich, um das Benutzerzertifikat von der Smartcard für die Netzwerkauthentifizierung abzurufen. Da SSO die PIN zwischenspeichert, kann das Zertifikat ohne Benutzereingriff abgerufen werden. Ohne einmaliges Anmelden müsste EAP-TLS erneut eine PIN-Sammlungsbenutzeroberfläche auslösen.

Einen schrittweisen Ansatz finden Sie unter [SSO EAP-TLS PIN Caching Behavior (Verhalten beim Zwischenspeichern von SSO-EAP-TLS-PIN).](sso-eap-tls-pin-caching-behavior-.md)

## <a name="sso-password-change-behavior"></a>SSO-Kennwortänderungsverhalten

Eine Unterstützung kann die Netzwerkauthentifizierung mithilfe einer kennwortbasierten EAP-Methode wie Microsoft Challenge Handshake Authentication Protocol Version 2.0 (MS-CHAPv2) versuchen, die für die Verwendung von WinLogin-Anmeldeinformationen konfiguriert ist. In diesem Szenario sammelt die Unterstützung einmal Benutzeranmeldeinformationen und stellt sie EAPHost für die Netzwerkauthentifizierung zur Verfügung. Nach erfolgreicher Netzwerkauthentifizierung verwendet die Suppliplizierung den gleichen Satz von Anmeldeinformationen für WinLogin.

Wenn jedoch Anmeldeinformationen wie das Benutzerkennwort während der Netzwerkauthentifizierung ohne SSO-fähige Unterstützung geändert wurden, führt der nachfolgende WinLogin-Aufruf zu einem Fehler. SSO behält die neuen Anmeldeinformationen bei und ermöglicht eine erfolgreiche WinLogin-Anmeldung ohne zusätzlichen Benutzereingriff.

Einen schrittweisen Ansatz finden Sie unter SSO Password Change Behavior ( [SSO-Kennwortänderungsverhalten).](sso-password-change-behavior-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




