---
description: Active Directory ist der Verzeichnisdienst für Windows und bildet die Grundlage für Windows verteilten Netzwerke.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Zugreifen auf Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a5e60899e07335795d9728045f1e53876b013bb62c85176479fa7953ac45d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131963"
---
# <a name="accessing-active-directory"></a>Zugreifen auf Active Directory

Active Directory ist der Verzeichnisdienst für Windows und bildet die Grundlage für Windows verteilten Netzwerke. Sie können Active Directory verwenden, um Objekte in einer Computernetzwerkdomäne zu suchen, z. B. Benutzer, Sicherheitsrichtlinien, Drucker, verteilte Komponenten und andere Ressourcen. Der Name Active Directory bezieht sich sowohl auf den Verzeichnisdienst als auch auf das Verzeichnis selbst.

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

 

Windows ermöglicht den Zugriff auf Active Directory über WMI, indem eine Reihe von Verweisen auf jede Klasse und jedes Objekt erstellt wird, die in Active Directory enthalten sind. Durch den Zugriff auf den Directory Services-Anbieter über WMI können Sie WMI-fähige Anwendungen erstellen, die auf die umfangreichen Informationen in Active Directory zugreifen können.

Mit diesen Schnittstellen haben Sie folgende Möglichkeiten:

-   Rufen Sie Klassen und Instanzen ab.
-   Aufzählen von Klassen und Instanzen.
-   Erstellen Sie neue Instanzen.
-   Ändern vorhandener Instanzen.
-   Löschen vorhandener Instanzen.
-   Abfragen von Active Directory.

Die folgenden Themen helfen Ihnen bei der Verwendung von Active Directory mit WMI:

-   [Verwenden der richtigen Active Directory-Syntax](using-the-proper-active-directory-syntax.md)
-   [Zuordnen von Active Directory zu WMI](mapping-active-directory-to-wmi.md)

 

 



