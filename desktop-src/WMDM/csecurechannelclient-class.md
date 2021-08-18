---
title: CSecureChannelClient-Klasse
description: CSecureChannelClient-Klasse
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Geräte-Manager,CSecureChannelClient-Klasse
- Geräte-Manager,CSecureChannelClient-Klasse
- Desktopanwendungen,CSecureChannelClient-Klasse
- Programmierreferenz,CSecureChannelClient-Klasse
- Referenz für Windows Media Geräte-Manager,CSecureChannelClient-Klasse
- CSecureChannelClient-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef469c1e7a73b04124850952ef0690bd18c82ecb3fc624d08df081b7b669637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585613"
---
# <a name="csecurechannelclient-class"></a>CSecureChannelClient-Klasse

Die **CSecureChannelClient-Klasse** ist eine Hilfsklasse (keine Schnittstelle), die es Anwendungen ermöglicht, sich selbst zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und MACs zu erstellen.

Die **CSecureChannelClient-Klasse** macht die folgenden Methoden verfügbar.



| Methode                                                            | BESCHREIBUNG                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Authentifizieren**](/previous-versions/ms983906(v=msdn.10))         | Löst den Austausch von Zertifikaten zwischen Komponenten aus, um eine Vertrauensstellung aufzubauen.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Entschlüsselt über einen Parameter empfangene Daten.                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Verschlüsselt Daten, die über einen Parameter gesendet werden.                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | Überprüft, ob ein sicherer Authentifizierungskanal erfolgreich eingerichtet wurde. Diese Methode wird nicht von Anwendungen verwendet. |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | Ruft die Anwendungssicherheitsebenen der lokalen und Remotekomponenten ab.                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | Ruft den aktuellen Sitzungsschlüssel ab. Diese Methode wird nicht von Anwendungen verwendet.                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | Gibt den MAC-Kanal (Message Authentication Code) frei und ruft einen endgültigen MAC-Wert ab.                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | Übernimmt einen MAC-Kanal (Message Authentication Code).                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | Fügt einem Nachrichtenauthentifizierungscode (MAC) einen Wert hinzu.                                                                      |
| [**Setcertificate**](/previous-versions/ms868504(v=msdn.10))     | Gibt das Zertifikat und den privaten Schlüssel des SAC-Clients (Secure Authenticated Channel) an.                               |
| [**SetInterface**](/previous-versions/bb231595(v=vs.85))         | Wählt die Schnittstelle aus, die für die Sichere Authentifizierungskanalkommunikation (SECURE Authenticated Channel, SAC) verwendet wird.                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | Legt den Sitzungsschlüssel fest, der für die Kommunikation mit einer anderen Komponente verwendet wird. Diese Methode wird nicht von Anwendungen verwendet.         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CSecureChannelServer-Klasse**](csecurechannelserver-class.md)
</dt> <dt>

[**IComponentAuthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Schnittstellen für Anwendungen**](interfaces-for-applications.md)
</dt> </dl>

 

 