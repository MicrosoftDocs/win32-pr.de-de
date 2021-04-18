---
title: Schnittstellen für sichere Inhaltsanbieter
description: Schnittstellen für sichere Inhaltsanbieter
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Referenz, DRM-geschützter Inhalt
- Referenz für Windows Media Device Manager, DRM-geschützten Inhalt
- DRM-geschützter Inhalt
- Windows Media Device Manager, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Device Manager, sicherer Inhaltsanbieter (Secure Content Provider, SCP)
- Programmier Referenz, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Referenz für Windows Media Device Manager, Secure Content Provider (SCP)
- Secure Content Provider (SCP)
- SCP (sicherer Inhaltsanbieter)
- Windows Media Device Manager, SCP-Schnittstellen
- Device Manager, SCP-Schnittstellen
- Programmier Referenz, SCP-Schnittstellen
- Referenz für Windows Media Device Manager, SCP-Schnittstellen
- SCP-Schnittstellen, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340624"
---
# <a name="interfaces-for-secure-content-providers"></a>Schnittstellen für sichere Inhaltsanbieter

Ein sicherer Inhaltsanbieter (Secure Content Provider, SCP) ist eine Plug-in-Komponente, die es Windows Media Device Manager ermöglicht, Rechte Informationen von DRM-geschützten Inhalten zu übertragen und anzufordern. Microsoft stellt eine SCP-Komponente bereit, die von DRM geschützte WMA-und WMV-Dateien verarbeiten kann. Wenn Ihr Gerät oder Ihre Anwendung DRM-geschützten Inhalt anderer Formate verwendet, sollte eine SCP-Komponente erstellt werden, indem alle diese Schnittstellen implementiert werden. Andernfalls müssen Sie diese Schnittstellen nicht verwenden.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iscpsecureauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | Die primäre Schnittstelle des sicheren Inhalts Anbieters.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Erweitert **iscpsecureauthenticate** durch Bereitstellen einer Möglichkeit, ein Sitzungs Objekt zu erhalten.                                                                                                                                                                       |
| [**Iscpsecureexchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Dient zum Austauschen geschützter Inhalte und Rechte, die mit Inhalten verknüpft sind.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Erweitert **iscpsecureexchange** durch Bereitstellen einer neuen Version der **transfercontainerdata** -Methode.                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Erweitert **ISCPSecureExchange2** durch eine verbesserte Datenaustausch Leistung und eine Übertragungs Complete-Rückruf Methode.                                                                                                                            |
| [**Iscpsecurequery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Wird von Windows Media Device Manager abgefragt, um den Besitz geschützter Inhalte zu ermitteln.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Erweitert **iscpsecurequery** durch Funktionalität, die bestimmt, ob der Anbieter für sichere Inhalte für den Inhalt zuständig ist, und wenn dies der Fall ist, die Bereitstellung einer URL zum Aktualisieren von widerrufenen Komponenten und zum Ermitteln der abrufenden Komponenten. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Erweitert **ISCPSecureQuery2** durch die Bereitstellung eines Satzes neuer Methoden zum Abrufen der Rechte und Treffen der Entscheidung für einen unverschlüsselten Kanal.                                                                                                                     |
| [**Iscpsession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Bietet eine effiziente allgemeine Zustands Verwaltung für mehrere Vorgänge.                                                                                                                                                                                  |



 

 

 




