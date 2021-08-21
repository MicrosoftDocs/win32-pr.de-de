---
title: Implementieren von Active Directory-Dienstanbietern
description: Active Directory-Dienstschnittstellen (ADSI) sind COM-Schnittstellen, die Verzeichnisdienstobjekte umschließen, um sie für Clients von Verzeichnisdiensten verfügbar zu machen. Durch die Bereitstellung einer Implementierung von ADSI erweitern Sie Ihre Clientbasis auf den Satz von ADSI-Clientanwendungen.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementieren von ADSI-Anbietern für Active Directory-Dienstanbieter
- Implementieren von ADSI-Anbietern ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3eb1275398a82a2ef179678e56cb9a7eda2e63eb4278906fc925fcb1d7cf6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427559"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implementieren von Active Directory-Dienstanbietern

Active Directory-Dienstschnittstellen (ADSI) sind COM-Schnittstellen, die Verzeichnisdienstobjekte umschließen, um sie für Clients von Verzeichnisdiensten verfügbar zu machen. Durch die Bereitstellung einer Implementierung von ADSI erweitern Sie Ihre Clientbasis auf den Satz von ADSI-Clientanwendungen.

Wie bei jeder COM-Implementierung können Sie einen ADSI-Anbieter in vielen Sprachen schreiben. Die ADSI COM-Schnittstellen sind als duale Schnittstellen definiert, die sowohl die Namensauflösung zur Laufzeit als auch zur Kompilierzeit ermöglichen. Sie können von Automation-kompatiblen Sprachen wie Visual Basic, Visual Basic Scripting Edition und den leistungs- und effizienzbewussteren Sprachen wie C und C++ aufgerufen werden. ADSI-Clients enthalten auch Webanwendungen, die Active Server Pages und Verwaltungs-Snap-Ins über die Microsoft Management Console.

Da ADSI einen eigenen anbieterdefinierten OLE DB, ermöglicht die Implementierung der von [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) definierten Suchfunktionen auch ADSI-Clients, Ihren Verzeichnisdienst nach Daten zu abfragen.

Alle Verzeichnisdienstobjekte können durch ein generisches ADSI-Objekt dargestellt werden, das [**IDirectoryObject unterstützt.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ADSI stellt die Bausteine zur Verfügung, die zur Darstellung der Features und Dienste eines beliebigen Verzeichnisdiensts erforderlich sind.

Darüber hinaus stellen die ADSI-Metaschnittstellen allgemeine Objekte dar, die von Verzeichnisadministratoren verwendet werden. Sie ordnen die Eigenschaften der Metaschnittstellen den Eigenschaften zu, die von Ihrem Verzeichnisdienst unterstützt werden. ADSI-Clients, die mit den Active Directory-Dienstschnittstellen programmieren, erhalten Zugriff auf Ihren Verzeichnisdienst, sobald der Anbieter installiert und das System neu gestartet wird.

Wenn Ihr Verzeichnisdienst eine Schemadarstellung unterstützt, ermöglicht die Unterstützung der Schemaverwaltungsschnittstellen den direkten Zugriff auf Ihren Namespace für Verzeichnisdienstbrowser. Durch die Veröffentlichung Ihrer Features über das Schema können Clients Ihren Verzeichnisdienst online abfragen und die von Ihnen angebotenen Dienste nutzen. Aufgrund der Onlineschemaverfügbarkeit und des COM-Schnittstellenvorteils können Sie ihrer Clientsoftware weiterhin neue Features zur Verfügung stellen, während Sie downlevelbasierte Versionen unterstützen.

 

 




