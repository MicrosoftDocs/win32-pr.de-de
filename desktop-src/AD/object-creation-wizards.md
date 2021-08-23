---
title: Objekterstellungs-Assistenten
description: In den administrativen MMC-Snap-Ins von Active Directory Domain Services kann der Benutzer neue Objekte in einem Verzeichnis erstellen, indem er das Kontextmenü für den Container öffnet, in dem das neue Objekt erstellt wird, Neu und die Klasse des zu erstellenden Objekts auswählt. Beim Erstellen neuer Instanzen eines Objekts wird der Objekterstellungs-Assistent gestartet. Jede Objektklasse kann die Verwendung eines bestimmten Erstellungs-Assistenten oder einen generischen Erstellungs-Assistenten angeben. Für allgemeine Klassen wie user und organizationalUnit stellt das Active Directory-Benutzer und -Computer-Snap-In einen Standardsatz von Erstellungs-Assistenten zur Bereitstellung. Es gibt zwei Möglichkeiten, einen Erstellungs-Assistenten zu erweitern. Ersetzen Sie einen vorhandenen Assistenten, oder geben Sie eine an, wenn eine für die Klasse nicht vorhanden ist. Der vorhandene Assistent wird ersetzt, indem eine Erweiterung für die Erstellung primärer Objekte erstellt wird. Eine primäre Erstellungserweiterung stellt den ersten Satz von Seiten zur Seite und wird auf die gleiche Weise gehostet wie native Seiten. Eine primäre Erstellungserweiterung unterstützt auch den Erweiterbarkeitsmechanismus, sodass andere Erweiterungen des Erstellungs-Assistenten aufgerufen werden können. Ein Beispiel für eine primäre Erweiterung finden Sie im scpwizard-Beispiel im Platform Software Development Kit (SDK). Erweitern eines vorhandenen Assistenten Ein vorhandener Assistent kann mit einer erweiterung für die Erstellung sekundärer Objekte erweitert werden. Eine sekundäre Erstellungserweiterung fügt Den nativen Seiten oder der primären Erweiterung Assistentenseiten hinzu. Weitere Informationen und ein Beispiel für eine sekundäre Erstellungserweiterung finden Sie im Beispiel userwizard im Platform SDK.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- Objekte AD , Erstellungs-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97c5c8f1b521d28c926d53830135dbb1b1fc907758e7047bc91c68856eedc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025587"
---
# <a name="object-creation-wizards"></a>Objekterstellungs-Assistenten

In den administrativen MMC-Snap-Ins von Active Directory Domain Services kann der Benutzer neue Objekte in einem Verzeichnis erstellen, indem er das Kontextmenü für den Container öffnet, in dem das neue Objekt erstellt wird. Wählen Sie Neu aus, und wählen Sie die Klasse des zu erstellenden Objekts aus. Beim Erstellen neuer Instanzen eines Objekts wird der Objekterstellungs-Assistent gestartet. Jede Objektklasse kann die Verwendung eines bestimmten Erstellungs-Assistenten oder einen generischen Erstellungs-Assistenten angeben. Für allgemeine Klassen, z. B. [**user**](/windows/desktop/ADSchema/c-user) und [**organizationalUnit,**](/windows/desktop/ADSchema/c-organizationalunit)stellt das Active Directory-Benutzer und -Computer-Snap-In einen Standardsatz von Erstellungs-Assistenten zur Bereitstellung.

Es gibt zwei Möglichkeiten, einen Erstellungs-Assistenten zu erweitern:

-   Ersetzen Sie einen vorhandenen Assistenten, oder geben Sie einen assistenten an, wenn dieser für die Klasse nicht vorhanden ist: Der vorhandene Assistent wird ersetzt, indem eine Primäre Objekterstellungserweiterung *erstellt wird.* Eine primäre Erstellungserweiterung stellt den ersten Satz von Seiten zur Seite und wird auf die gleiche Weise gehostet wie native Seiten. Eine primäre Erstellungserweiterung unterstützt auch den Erweiterbarkeitsmechanismus, sodass andere Erweiterungen des Erstellungs-Assistenten aufgerufen werden können. Ein Beispiel für eine primäre Erweiterung finden Sie im scpwizard-Beispiel im Platform Software Development Kit (SDK).
-   Erweitern eines vorhandenen Assistenten: Ein vorhandener Assistent kann mit einer sekundären *Objekterstellungserweiterung erweitert werden.* Eine sekundäre Erstellungserweiterung fügt Den nativen Seiten oder der primären Erweiterung Assistentenseiten hinzu. Weitere Informationen und ein Beispiel für eine sekundäre Erstellungserweiterung finden Sie im Beispiel userwizard im Platform SDK.

## <a name="developer-audience"></a>Entwicklerzielgruppe

In dieser Dokumentation wird davon ausgegangen, dass der Leser mit der COM-Vorgangs- und Komponentenentwicklung mit C++ vertraut ist. Es ist derzeit nicht möglich, eine Erweiterung für den Active Directory-Objekterstellungs-Assistenten mithilfe von Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Erstellen einer Active Directory-Objekterstellungserweiterung

Sowohl primäre als auch sekundäre Objekterstellungserweiterungen sind COM-In-Proc-Server, die bestimmte Schnittstellen implementieren und bei Active Directory Domain Services.

**So erstellen und installieren Sie eine Objekterstellungserweiterung**

1.  Erstellen Sie die Erweiterungs-DLL für die Objekterstellung. Eine Objekterstellungserweiterung ist ein COM-In-Proc-Server, der mindestens die [**IDsAdminNewObjExt-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) implementiert. Weitere Informationen finden Sie unter [Implementing the Object Creation Extension COM Object](implementing-the-object-creation-extension-com-object.md).
2.  Installieren Sie die Erstellungserweiterung auf Computern, auf denen die Erstellungserweiterung verwendet werden soll. Erstellen Sie hierzu ein Microsoft Windows Installer-Paket für die Erweiterungs-DLL für die Erstellung, und stellen Sie das Paket entsprechend mithilfe der Gruppenrichtlinie zur Verfügung. Weitere Informationen finden Sie unter [Verteilen Benutzeroberfläche -Komponenten.](distributing-user-interface-components.md)
3.  Registrieren Sie die Erstellungserweiterung in Windows Registrierung und Active Directory Domain Services. Weitere Informationen finden Sie unter [Registrieren der Objekterstellungserweiterung.](registering-the-object-creation-extension.md)

## <a name="using-an-object-creation-wizard"></a>Verwenden eines Objekterstellungs-Assistenten

Ein Objekterstellungs-Assistent kann auch von einer anderen Anwendung als den administrativen MMC-Snap-Ins der Active Directory Domain Services. Weitere Informationen finden Sie unter [Aufrufen von Erstellungs-Assistenten aus Ihrer Anwendung.](invoking-creation-wizards-from-your-application.md)

Wenn kein Erstellungs-Assistent für eine Objektklasse registriert ist, stellen die administrativen Snap-Ins einen generischen Erstellungs-Assistenten zur Verfügung. Der Assistent für die generische Erstellung wird zur Laufzeit aus der Liste der obligatorischen Eigenschaften für die Klasse des erstellten Objekts erstellt. Für jede obligatorische Eigenschaft wird der Benutzeroberfläche eine Seite hinzugefügt. Der Assistent für die generische Erstellung ist nicht erweiterbar. Wenn Erweiterbarkeit erforderlich ist, muss sie durch eine Primäre Objekterstellungserweiterung ersetzt werden.

 

 