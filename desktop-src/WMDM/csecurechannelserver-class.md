---
title: Csecurechannelserver-Klasse
description: Csecurechannelserver-Klasse
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Device Manager, csecurechannelserver-Klasse
- Device Manager, csecurechannelserver-Klasse
- Dienstanbieter, csecurechannelserver-Klasse
- Programmier Referenz, csecurechannelserver-Klasse
- Referenz für Windows Media Device Manager, csecurechannelserver-Klasse
- Csecurechannelserver-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727880"
---
# <a name="csecurechannelserver-class"></a>Csecurechannelserver-Klasse

Die **csecurechannelserver** -Klasse ist eine Hilfsklasse (keine Schnittstelle), die einem Dienstanbieter oder einem sicheren Inhaltsanbieter ermöglicht, eine Anwendung mithilfe der [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und Mac-Signaturen zu erstellen. Der Authentifizierungsprozess erfordert, dass die Anwendung ein **csecurechannelclient** -Objekt erstellt und dass der Dienstanbieter ein **csecurechannelserver** -Objekt erstellt. Die **csecurechannelclient** -Klasse und die **csecurechannelserver** -Klasse werden in der statischen Link Bibliothek "mssachlp. lib" deklariert. Alle Methoden der Schnittstellen von Windows Media Device Manager, Service Provider und Secure Content Provider können WMDM \_ E \_ notcertified zurückgeben, um anzugeben, dass der Aufrufer nicht erfolgreich authentifiziert wurde.

Die **csecurechannelserver** -Klasse stellt die folgenden Methoden zur Verfügung.



| Methode                                                            | BESCHREIBUNG                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Decryptparam**](/previous-versions/bb231598(v=vs.85))         | Entschlüsselt die Daten, die in einem Parameter enthalten sind.                                                 |
| [**Verschlüsseltparam**](/previous-versions/ms868509(v=msdn.10))         | Verschlüsselt die Daten, die in einem Parameter enthalten sind.                                                 |
| [**fisauthenticated**](/previous-versions/bb231600(v=vs.85)) | Mit dieser Option wird überprüft, ob ein sicherer Authentifizierungs Kanal erfolgreich eingerichtet wurde.            |
| [**Getappsec**](/previous-versions/bb231601(v=vs.85))               | Ruft die Anwendungs Sicherheitsgrade der lokalen Komponenten und Remote Komponenten ab.               |
| [**Getessionkey**](/previous-versions/bb231602(v=vs.85))       | Ruft den aktuellen Sitzungsschlüssel ab.                                                          |
| [**Macfinal**](/previous-versions/ms868513(v=msdn.10))                 | Gibt den Mac-Kanal (Message Authentication Code) frei und Ruft einen abschließenden Mac-Wert ab.     |
| [**Macinit**](/previous-versions/ms868514(v=msdn.10))                   | Ruft einen Mac-Kanal (Message Authentication Code) ab.                                       |
| [**Macupdate**](/previous-versions/ms868515(v=msdn.10))               | Aktualisiert den Mac-Wert (Message Authentication Code) mit einem Parameterwert.                 |
| [**Sacauth**](/previous-versions/ms868516(v=msdn.10))                   | Legt einen sicheren authentifizierten Kanal zwischen Komponenten fest.                              |
| [**Sacgetprotokolle**](/previous-versions/ms868517(v=msdn.10))   | Meldet die Protokolle, die von einer Komponente unterstützt werden.                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | Gibt das Zertifikat und den privaten Schlüssel des SAC-Servers (Secure authentifiziert Channel) an. |
| [**"-Essionkey"**](/previous-versions/ms868519(v=msdn.10))       | Legt den Sitzungsschlüssel fest, der für die Kommunikation mit einer anderen Komponente verwendet wird.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Csecurechannelclient-Klasse**](csecurechannelclient-class.md)
</dt> <dt>

[**Icomponentauthenticate-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Schnittstellen für Dienstanbieter**](interfaces-for-service-providers.md)
</dt> <dt>

[**Verwenden sicherer authentifizierter Kanäle**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 