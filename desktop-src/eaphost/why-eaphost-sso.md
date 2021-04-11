---
title: SSO-EAPHost-Szenarioübersicht
description: Enthält zwei Szenarien, in denen die Vorteile eines aktivierten Supplicant (Single Sign-on, einmaliges Anmelden) aufgezeigt werden.
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101126"
---
# <a name="sso-eaphost-scenario-overview"></a>SSO-EAPHost-Szenarioübersicht

Das folgende Thema enthält zwei Szenarien, in denen die Vorteile eines aktivierten Supplicant (Single Sign-on, einmaliges Anmelden) veranschaulicht werden.

## <a name="about-the-scenarios"></a>Informationen zu den Szenarien

SSO stellt Funktionen bereit, um zusätzliche Benutzer Anmelde Informationen zu erhalten, als normalerweise im EAP-benutzerblob gespeichert werden. Im Gegensatz zu anderen Anmelde Informationsprozessen können von SSO aktivierte Supplicants Anmelde Situationen wie das AP-Roaming und die Kenn Wort Änderung ohne Benutzereingriff auflösen.

## <a name="sso-eap-tls-pin-caching-behavior"></a>SSO EAP-TLS Pin Caching-Verhalten

Ein Supplicant kann die Netzwerk Authentifizierung mit einer Smartcard-basierten EAP-Methode wie z. b. EAP-TLS (Extensible Authentication Protocol Transport Layer Security) versuchen. In diesem und ähnlichen Szenario erhält der Supplicant die Smartcard-PIN vom Benutzer und ruft ein Benutzerzertifikat für die Netzwerk Authentifizierung ab, gefolgt von einem Windows-Anmelde Namen auf dem lokalen Computer. Nach erfolgreicher Authentifizierung speichert der Supplicant den benutzerblob zwischen und speichert keine Benutzer-PIN-Informationen.

Wenn der Benutzer zu einem anderen Speicherort wechselt, müssen Wiederaufnahme-und erneute Authentifizierung erfolgen. Da das Zertifikat nicht vor der Anmeldung gespeichert werden kann, schlägt die Benutzerauthentifizierung fehl, und der Benutzer-BLOB wird vom Supplicant geleert. An diesem Punkt ist die Benutzer-PIN erforderlich, um das Benutzerzertifikat für die Netzwerk Authentifizierung von der Smartcard abzurufen. Da SSO die PIN zwischenspeichert, kann das Zertifikat ohne Benutzereingriff abgerufen werden. Ohne SSO müsste EAP-TLS erneut eine Benutzeroberfläche für die PIN-Erfassung aufrufen.

Eine schrittweise Vorgehensweise finden Sie unter [SSO EAP-TLS Pin Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).

## <a name="sso-password-change-behavior"></a>Verhalten von SSO-Kenn Wort Änderungen

Ein Supplicant kann die Netzwerk Authentifizierung mit einer Kenn Wort basierten EAP-Methode wie Microsoft Challenge Handshake Authentication Protocol, Version 2,0 (MS-CHAPv2), verwenden, die für die Verwendung von winlogin-Anmelde Informationen konfiguriert ist. In diesem Szenario sammelt das Supplicant-Benutzer Anmelde Informationen einmal und stellt Sie für die Netzwerk Authentifizierung per EAPHost bereit. Nach erfolgreicher Netzwerk Authentifizierung verwendet der Supplicant denselben Satz von Anmelde Informationen für winlogin.

Wenn Anmelde Informationen, z. b. das Benutzer Kennwort, während der Netzwerk Authentifizierung ohne aktivierten Supplicant geändert wurden, führt der nachfolgende winlogin-Befehl zu einem Fehler. SSO behält die neuen Anmelde Informationen bei und ermöglicht einen erfolgreichen winlogin-Vorgang ohne zusätzlichen Benutzereingriff.

Eine Schritt-für-Schritt-Vorgehensweise finden Sie unter SSO-Kenn [Wort Änderungs Verhalten](sso-password-change-behavior-.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SSO und PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




