---
title: Assistenten zum Erstellen von Objekten
description: In den Verwaltungs-MMC-Snap-Ins von Active Directory Domain Services kann der Benutzer neue Objekte in einem Verzeichnis erstellen, indem er das Kontextmenü für den Container öffnet, in dem das neue Objekt erstellt wird, und dann neu und die Klasse des zu erstellenden Objekts auswählen. Beim Erstellen neuer Instanzen eines Objekts wird der Objekterstellungs-Assistent gestartet. Jede Objektklasse kann die Verwendung eines bestimmten Erstellungs-Assistenten angeben, oder es kann ein generischer Erstellungs-Assistent verwendet werden. Für allgemeine Klassen, wie z. b. User und OrganizationalUnit, stellt das Snap-in "Active Directory-Benutzer und-Computer" einen Standardsatz von Assistenten für die Erstellung bereit. Es gibt zwei Möglichkeiten, einen Erstellungs-Assistenten zu erweitern, der einen vorhandenen Assistenten ersetzt, oder einen vorhandenen Assistenten bereitzustellen, wenn er für die Klasse nicht vorhanden ist. der vorhandene Assistent wird durch Erstellen einer Erweiterung für das primäre Objekt erstellen ersetzt. Eine primäre Erstellungs Erweiterung stellt die erste Gruppe von Seiten bereit und wird auf die gleiche Weise wie Native Seiten gehostet. Eine primäre Erstellungs Erweiterung unterstützt auch den Erweiterbarkeits Mechanismus, sodass andere Erweiterungen des Assistenten zum Erstellen von Erweiterungen aufgerufen werden können. Ein Beispiel für eine primäre Erweiterung finden Sie im scpwizard-Beispiel im Platform Software Development Kit (SDK). Erweitern eines vorhandenen Assistenten ein vorhandener Assistent kann mit einer sekundären Objekt Erstellungs Erweiterung erweitert werden. Eine sekundäre Erstellungs Erweiterung fügt der systemeigenen Seite oder der primären Erweiterung Assistenten Seiten hinzu. Weitere Informationen und ein Beispiel für eine sekundäre Erstellungs Erweiterung finden Sie unter dem userwizard-Beispiel im Platform SDK.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- Objekte AD, Assistenten für die Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc3dbacaf6eee5670fdacd9a587a497397c4d1b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101442"
---
# <a name="object-creation-wizards"></a>Assistenten zum Erstellen von Objekten

In den Verwaltungs-MMC-Snap-Ins von Active Directory Domain Services kann der Benutzer neue Objekte in einem Verzeichnis erstellen, indem er das Kontextmenü für den Container öffnet, in dem das neue Objekt erstellt wird, und dann **neu** und die Klasse des zu erstellenden Objekts auswählen. Beim Erstellen neuer Instanzen eines Objekts wird der Objekterstellungs-Assistent gestartet. Jede Objektklasse kann die Verwendung eines bestimmten Erstellungs-Assistenten angeben, oder es kann ein generischer Erstellungs-Assistent verwendet werden. Für allgemeine Klassen, wie z. b. [**User**](/windows/desktop/ADSchema/c-user) und [**OrganizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit), stellt das Snap-in "Active Directory-Benutzer und-Computer" einen Standardsatz von Assistenten für die Erstellung bereit.

Es gibt zwei Möglichkeiten, einen Erstellungs-Assistenten zu erweitern:

-   Ersetzen Sie einen vorhandenen Assistenten, oder geben Sie einen an, wenn dieser nicht für die Klasse vorhanden ist: der vorhandene Assistent wird durch Erstellen einer Erweiterung für die *Erstellung eines primären Objekts* ersetzt. Eine primäre Erstellungs Erweiterung stellt die erste Gruppe von Seiten bereit und wird auf die gleiche Weise wie Native Seiten gehostet. Eine primäre Erstellungs Erweiterung unterstützt auch den Erweiterbarkeits Mechanismus, sodass andere Erweiterungen des Assistenten zum Erstellen von Erweiterungen aufgerufen werden können. Ein Beispiel für eine primäre Erweiterung finden Sie im scpwizard-Beispiel im Platform Software Development Kit (SDK).
-   Erweitern eines vorhandenen Assistenten: ein vorhandener Assistent kann mit einer *sekundären Objekt Erstellungs Erweiterung* erweitert werden. Eine sekundäre Erstellungs Erweiterung fügt der systemeigenen Seite oder der primären Erweiterung Assistenten Seiten hinzu. Weitere Informationen und ein Beispiel für eine sekundäre Erstellungs Erweiterung finden Sie unter dem userwizard-Beispiel im Platform SDK.

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Reader mit der com-Operation und-Komponentenentwicklung mit C++ vertraut ist. Es ist derzeit nicht möglich, eine Erweiterung für den Assistenten zum Erstellen von Active Directory Objekten mithilfe von Visual Basic zu erstellen.

## <a name="creating-an-active-directory-object-creation-extension"></a>Erstellen einer Erweiterung zum Erstellen von Active Directory Objekten

Bei der Erstellung von primären und sekundären Objekten handelt es sich um com-in-proc-Server, die bestimmte Schnittstellen implementieren und bei Active Directory Domain Services registriert sind.

**So erstellen und installieren Sie eine Erweiterung zur Objekt Erstellung**

1.  Erstellen Sie die Erweiterungs-DLL für die Objekt Erstellung. Eine Objekt Erstellungs Erweiterung ist ein com-in-proc-Server, der mindestens die [**idsadminnewobjext**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) -Schnittstelle implementiert. Weitere Informationen finden Sie unter [Implementieren der Objekt Erstellungs Erweiterung com-Objekt](implementing-the-object-creation-extension-com-object.md).
2.  Installieren Sie die Erstellungs Erweiterung auf Computern, auf denen die Erstellungs Erweiterung verwendet werden soll. Erstellen Sie zu diesem Zweck ein Microsoft Windows Installer Paket für die Erweiterungs-DLL, und stellen Sie das Paket entsprechend mithilfe der Gruppenrichtlinie bereit. Weitere Informationen finden Sie unter [Verteilen von Benutzeroberflächen Komponenten](distributing-user-interface-components.md).
3.  Registrieren Sie die Erstellungs Erweiterung in der Windows-Registrierung und mit Active Directory Domain Services. Weitere Informationen finden Sie unter [Registrieren der Objekt Erstellungs Erweiterung](registering-the-object-creation-extension.md).

## <a name="using-an-object-creation-wizard"></a>Verwenden eines Objekterstellungs-Assistenten

Ein Objekterstellungs-Assistent kann auch von einer anderen Anwendung als den MMC-Snap-Ins für die Verwaltung von Active Directory Domain Services aufgerufen werden. Weitere Informationen finden Sie unter [Aufrufen von Erstellungs-Assistenten aus Ihrer Anwendung](invoking-creation-wizards-from-your-application.md).

Wenn ein Erstellungs-Assistent für eine Objektklasse nicht registriert ist, stellen die Verwaltungs-Snap-Ins einen Assistenten für die generische Erstellung bereit. Der Assistent für die generische Erstellung wird zur Laufzeit aus der Liste der obligatorischen Eigenschaften für die Objektklasse erstellt, die erstellt wurde. Für jede obligatorische Eigenschaft wird der Benutzeroberfläche eine Seite hinzugefügt. Der Assistent für die generische Erstellung ist nicht erweiterbar. Wenn die Erweiterbarkeit erforderlich ist, muss Sie durch eine primäre Objekt Erstellungs Erweiterung ersetzt werden.

 

 