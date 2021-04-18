---
title: Csecurechannelclient-Klasse
description: Csecurechannelclient-Klasse
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Device Manager, csecurechannelclient-Klasse
- Device Manager, csecurechannelclient-Klasse
- Desktop Anwendungen, csecurechannelclient-Klasse
- Programmier Referenz, csecurechannelclient-Klasse
- Referenz für Windows Media Device Manager, csecurechannelclient-Klasse
- Csecurechannelclient-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337439"
---
# <a name="csecurechannelclient-class"></a>Csecurechannelclient-Klasse

Die **csecurechannelclient** -Klasse ist eine Hilfsklasse (keine Schnittstelle), die es Anwendungen ermöglicht, sich selbst zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und Macs zu erstellen.

Die **csecurechannelclient** -Klasse stellt die folgenden Methoden zur Verfügung.



| Methode                                                            | BESCHREIBUNG                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Authenticate**](/previous-versions/ms983906(v=msdn.10))         | Hiermit wird der Austausch von Zertifikaten zwischen Komponenten ausgelöst, um eine Vertrauensstellung einzurichten.                                              |
| [**Decryptparam**](/previous-versions/bb231586(v=vs.85))         | Entschlüsselt Daten, die über einen Parameter empfangen werden.                                                                               |
| [**Verschlüsseltparam**](/previous-versions/bb231587(v=vs.85))         | Verschlüsselt Daten, die über einen Parameter gesendet werden.                                                                         |
| [**fisauthenticated**](/previous-versions/ms868497(v=msdn.10)) | Mit dieser Option wird überprüft, ob ein sicherer Authentifizierungs Kanal erfolgreich eingerichtet wurde. Diese Methode wird von Anwendungen nicht verwendet. |
| [**Getappsec**](/previous-versions/ms868498(v=msdn.10))               | Ruft die Anwendungs Sicherheitsgrade der lokalen Komponenten und Remote Komponenten ab.                                             |
| [**Getessionkey**](/previous-versions/bb231590(v=vs.85))       | Ruft den aktuellen Sitzungsschlüssel ab. Diese Methode wird von Anwendungen nicht verwendet.                                               |
| [**Macfinal**](/previous-versions/bb231591(v=vs.85))                 | Gibt den Mac-Kanal (Message Authentication Code) frei und Ruft einen abschließenden Mac-Wert ab.                                   |
| [**Macinit**](/previous-versions/bb231592(v=vs.85))                   | Ruft einen Mac-Kanal (Message Authentication Code) ab.                                                                     |
| [**Macupdate**](/previous-versions/bb231593(v=vs.85))               | Fügt einem Nachrichten Authentifizierungscode (Message Authentication Code, Mac) einen Wert hinzu.                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | Gibt das Zertifikat und den privaten Schlüssel des SAC-Clients (Secure authentifiziert Channel) an.                               |
| [**Setinterface**](/previous-versions/bb231595(v=vs.85))         | Wählt die für Secure authentifiziert Channel (SAC)-Kommunikation verwendete Schnittstelle aus.                                         |
| [**"-Essionkey"**](/previous-versions/ms868506(v=msdn.10))       | Legt den Sitzungsschlüssel fest, der für die Kommunikation mit einer anderen Komponente verwendet wird. Diese Methode wird von Anwendungen nicht verwendet.         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Csecurechannelserver-Klasse**](csecurechannelserver-class.md)
</dt> <dt>

[**Icomponentauthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Schnittstellen für Anwendungen**](interfaces-for-applications.md)
</dt> </dl>

 

 