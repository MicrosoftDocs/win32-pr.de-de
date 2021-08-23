---
title: Schnittstellen für sichere Inhaltsanbieter
description: Schnittstellen für sichere Inhaltsanbieter
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Medien Geräte-Manager, DRM-geschützte Inhalte
- Geräte-Manager, DRM-geschützter Inhalt
- Programmierreferenz, DRM-geschützter Inhalt
- Referenz für Windows Media Geräte-Manager,DRM-geschützte Inhalte
- DRM-geschützter Inhalt
- Windows Media Geräte-Manager,Secure Content Provider (SCP)
- Geräte-Manager, sicherer Inhaltsanbieter (Secure Content Provider, SCP)
- Programmierreferenz,Sicherer Inhaltsanbieter (Secure Content Provider, SCP)
- Referenz für Windows Media Geräte-Manager,Secure Content Provider (SCP)
- Secure Content Provider (SCP)
- SCP (Sicherer Inhaltsanbieter)
- Windows Media Geräte-Manager,SCP-Schnittstellen
- Geräte-Manager,SCP-Schnittstellen
- Programmierreferenz, SCP-Schnittstellen
- Referenz für Windows Media Geräte-Manager,SCP-Schnittstellen
- SCP-Schnittstellen, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80b74cfc50fb6dcf328379c5c46696dc2ee097e2ed5c2507a2a4f14676efd85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119247340"
---
# <a name="interfaces-for-secure-content-providers"></a>Schnittstellen für sichere Inhaltsanbieter

Ein sicherer Inhaltsanbieter (Secure Content Provider, SCP) ist eine Plug-In-Komponente, die es Windows Media Geräte-Manager ermöglicht, Rechteinformationen von DRM-geschützten Inhalten zu übertragen und anzufordern. Microsoft stellt eine SCP-Komponente bereit, die DRM-geschützte WMA- und WMV-Dateien verarbeiten kann. Wenn Ihr Gerät oder Ihre Anwendung DRM-geschützte Inhalte anderer Formate verwendet, sollte eine SCP-Komponente erstellt werden, indem alle diese Schnittstellen implementiert werden. Andernfalls müssen Sie diese Schnittstellen nicht verwenden.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | Die primäre Schnittstelle des anbietersicheren Inhalts.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Erweitert **ISCPSecureAuthenticate,** indem eine Möglichkeit zum Abrufen eines Sitzungsobjekts zur Verfügung gestellt wird.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Wird verwendet, um geschützte Inhalte und Rechte auszutauschen, die inhalten zugeordnet sind.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Erweitert **ISCPSecureExchange** durch Bereitstellen einer neuen Version der **TransferContainerData-Methode.**                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Erweitert **ISCPSecureExchange2** durch verbesserte Datenaustauschleistung und eine vollständige Rückrufmethode für die Übertragung.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Wird von Windows Media Geräte-Manager abgefragt, um den Besitz geschützter Inhalte zu bestimmen.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Erweitert **ISCPSecureQuery** durch Funktionen, mit denen bestimmt wird, ob der sichere Inhaltsanbieter für den Inhalt verantwortlich ist. Wenn dies der Fall ist, wird eine URL zum Aktualisieren gesperrter Komponenten und zum Bestimmen der gesperrten Komponenten zur Verfügung gestellt. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Erweitert **ISCPSecureQuery2,** indem eine Reihe neuer Methoden zum Abrufen der Rechte und zum Treffen von Entscheidungen in einem eindeutigen Kanal zur Verfügung gestellt wird.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Stellt eine effiziente allgemeine Zustandsverwaltung für mehrere Vorgänge bereit.                                                                                                                                                                                  |



 

 

 




