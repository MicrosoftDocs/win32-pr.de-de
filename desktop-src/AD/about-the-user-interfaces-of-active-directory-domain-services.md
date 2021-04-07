---
title: Informationen zu den Benutzeroberflächen von Active Directory Domain Services
description: Administratoren und Benutzer müssen in der Lage sein, Verzeichnisdienst Objekte in Microsoft Active Directory Domain Services über eine Benutzeroberfläche anzuzeigen und zu ändern.
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c451a44660aaadbf0021ff57e675736b797d8f3e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038721"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>Informationen zu den Benutzeroberflächen von Active Directory Domain Services

Administratoren und Benutzer müssen in der Lage sein, Verzeichnisdienst Objekte in Microsoft Active Directory Domain Services über eine Benutzeroberfläche anzuzeigen und zu ändern. Administratoren verwalten den Active Directory Server mithilfe verschiedener MMC-Snap-Ins (Microsoft Management Console), insbesondere der Active Directory Domain Services Benutzer und Computer, Active Directory Domain Services Sites und Dienste, Active Directory Domain Services Domänen und Vertrauens Stellungen und Active Directory Domain Services Schema-Manager-Snap-Ins. Der Endbenutzer kann, wenn er die entsprechenden Berechtigungen erhält, auch das Active Directory MMC-Snap-Ins verwenden, um Verzeichnisobjekte anzuzeigen. Die Windows-Shell kann auch zum Anzeigen von Verzeichnis Objekten verwendet werden. Die Windows-Shell ermöglicht Benutzern das Durchsuchen von im Verzeichnis gespeicherten Objekten entweder vom Verzeichnis Element an den Netzwerk Orten auf dem Desktop oder über die Such Dialogfelder, die im Startmenü verfügbar sind.

Active Directory Domain Services unterstützen eine Benutzeroberfläche, die sich angepasst, um den Anforderungen von Administratoren und Endbenutzern gerecht zu werden. Mit Active Directory Domain Services können Sie die Benutzeroberfläche erweitern, die vorhandene Objektklassen darstellt, sowie neue Klassen, die dem Schema hinzugefügt werden. Die folgenden Elemente können verwendet werden, um die Benutzeroberfläche für jede im Schema definierte Klasse zu steuern oder zu erweitern:

-   [Eigenschaften Seiten für die Verwendung mit Anzeige spezifiken](property-pages-for-use-with-display-specifiers.md)
-   [Kontextmenüs für die Verwendung mit Anzeige spezifiken](context-menus-for-use-with-display-specifiers.md)
-   [Klassen-und Attribut anzeigen Amen](class-and-attribute-display-names.md)
-   [Assistenten zum Erstellen von Objekten](object-creation-wizards.md)
-   [Klassen Symbole](class-icons.md)
-   [Anzeigen von Containern als Blattknoten](viewing-containers-as-leaf-nodes.md)

Ab Windows 2000 stellt das System com-Objekte bereit, die allgemeine Dialogfelder zum Arbeiten mit Verzeichnis Objekten implementieren. In diesen Dialogfeldern wird eine gemeinsame Benutzeroberfläche bereitgestellt, ohne dass diese Dialogfelder neu implementiert werden müssen.

-   [Verzeichnis Objektauswahl](directory-object-picker.md)
-   [Domänen Browser](domain-browser.md)
-   [Container Browser](container-browser.md)

Active Directory Verwaltungs-Snap-Ins, Kontextmenüs und Eigenschaften Seiten können mithilfe von MMC-Erweiterungs-Snap-Ins erweitert werden. Andere MMC-Erweiterungen, z. b. Taskpads, Namespace Elemente, Steuer leisten und Symbolleisten können ebenfalls implementiert werden. Weitere Informationen finden Sie unter [Erweitern der Active Directory Verwaltungs-Snap-Ins](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins).

 

 