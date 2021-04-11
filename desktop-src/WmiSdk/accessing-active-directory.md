---
description: Active Directory ist der Verzeichnisdienst für Windows und ist die Grundlage für verteilte Windows-Netzwerke.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Zugreifen auf Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217969"
---
# <a name="accessing-active-directory"></a>Zugreifen auf Active Directory

Active Directory ist der Verzeichnisdienst für Windows und ist die Grundlage für verteilte Windows-Netzwerke. Sie können Active Directory verwenden, um Objekte in einer Computernetzwerk Domäne wie z. b. Benutzer, Sicherheitsrichtlinien, Drucker, verteilte Komponenten und andere Ressourcen zu suchen. Der Name Active Directory verweist sowohl auf den Verzeichnisdienst als auch auf das Verzeichnis selbst.

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

 

Windows macht Active Directory über WMI zugänglich, indem eine Reihe von Verweisen auf alle Klassen und Objekte erstellt werden, die in Active Directory enthalten sind. Durch den Zugriff auf den Verzeichnisdienst Anbieter über WMI können Sie WMI-fähige Anwendungen erstellen, die auf die umfangreichen Informationen zugreifen können, die in Active Directory enthalten sind.

Mit diesen Schnittstellen können Sie folgende Aktionen ausführen:

-   Abrufen von Klassen und Instanzen.
-   Auflisten von Klassen und Instanzen.
-   Erstellen Sie neue Instanzen.
-   Ändern vorhandener Instanzen.
-   Löschen Sie vorhandene Instanzen.
-   Abfrage Active Directory.

Die folgenden Themen unterstützen Sie bei der Verwendung von Active Directory mit WMI:

-   [Verwenden der richtigen Active Directory Syntax](using-the-proper-active-directory-syntax.md)
-   [Zuordnung von Active Directory zu WMI](mapping-active-directory-to-wmi.md)

 

 



