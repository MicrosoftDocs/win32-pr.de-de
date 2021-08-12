---
title: CSecureChannelServer-Klasse
description: CSecureChannelServer-Klasse
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Geräte-Manager,CSecureChannelServer-Klasse
- Geräte-Manager,CSecureChannelServer-Klasse
- Dienstanbieter,CSecureChannelServer-Klasse
- Programmierreferenz,CSecureChannelServer-Klasse
- Referenz für Windows Media Geräte-Manager,CSecureChannelServer-Klasse
- CSecureChannelServer-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87627fcdee6da42927ab88411dd579225dc38f025ae73bf9f4fe787c0c5e44bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585484"
---
# <a name="csecurechannelserver-class"></a>CSecureChannelServer-Klasse

Die **CSecureChannelServer-Klasse** ist eine Hilfsklasse (keine Schnittstelle), die es einem Dienstanbieter oder einem sicheren Inhaltsanbieter ermöglicht, eine Anwendung über die [**IComponentAuthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und MAC-Signaturen zu erstellen. Der Authentifizierungsprozess erfordert, dass die Anwendung ein **CSecureChannelClient-Objekt** erstellt und dass der Dienstanbieter ein **CSecureChannelServer-Objekt** erstellt. Die **Klassen CSecureChannelClient** und **CSecureChannelServer** werden in der statischen Linkbibliothek Mssachlp.lib deklariert. Alle Methoden von Windows Media Geräte-Manager, Dienstanbieter und sicheren Inhaltsanbieterschnittstellen können WMDM E NOTCERTIFIED zurückgeben, um anzugeben, dass der Aufrufer nicht erfolgreich authentifiziert \_ \_ wurde.

Die **CSecureChannelServer-Klasse** macht die folgenden Methoden verfügbar.



| Methode                                                            | BESCHREIBUNG                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | Entschlüsselt die in einem -Parameter enthaltenen Daten.                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | Verschlüsselt die in einem -Parameter enthaltenen Daten.                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | Überprüft, ob ein sicherer Authentifizierungskanal erfolgreich eingerichtet wurde.            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | Ruft die Anwendungssicherheitsebenen der lokalen und Remotekomponenten ab.               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | Ruft den aktuellen Sitzungsschlüssel ab.                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | Gibt den MAC-Kanal (Message Authentication Code) frei und ruft einen endgültigen MAC-Wert ab.     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | Übernimmt einen MAC-Kanal (Message Authentication Code).                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | Aktualisiert den Wert des Nachrichtenauthentifizierungscodes (Message Authentication Code, MAC) mit einem Parameterwert.                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | Richtet einen sicheren authentifizierten Kanal zwischen Komponenten ein.                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | Meldet die protokolle, die von einer Komponente unterstützt werden.                                             |
| [**Setcertificate**](/previous-versions/ms868518(v=msdn.10))     | Gibt das Zertifikat und den privaten Schlüssel des SAC-Servers (Secure Authenticated Channel) an. |
| [**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))       | Legt den Sitzungsschlüssel fest, der für die Kommunikation mit einer anderen Komponente verwendet wird.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CSecureChannelClient-Klasse**](csecurechannelclient-class.md)
</dt> <dt>

[**IComponentAuthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Schnittstellen für Dienstanbieter**](interfaces-for-service-providers.md)
</dt> <dt>

[**Verwenden von sicheren authentifizierten Kanälen**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 