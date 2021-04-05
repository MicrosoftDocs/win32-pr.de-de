---
description: Dieser Abschnitt enthält konzeptionelle Informationen, die für die Implementierung, Erweiterung und das Testen von Protokoll Handlern erforderlich sind.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Entwickeln von Protokoll Handlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750425"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>Entwickeln von Protokoll Handlern für Windows Search

Dieser Abschnitt enthält konzeptionelle Informationen, die für die Implementierung, Erweiterung und das Testen von Protokoll Handlern erforderlich sind.

-   [Grundlegendes zu Protokoll Handlern](-search-3x-wds-extidx-prot-implementing.md)
-   [Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md)
-   [Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
-   [Code Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
-   [Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md)
-   [Erstellen eines Suchconnector für einen Protokoll Handler](-search-3x-wds-ph-search-connector.md)
-   [Debuggen von Protokoll Handlern](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>Weitere Ressourcen

Konzeptionelle Hintergrundinformationen zur Indizierung finden Sie in den folgenden Themen:

-   Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
-   Informationen zum Erweitern von Windows Search zum Indizieren des Inhalts und der Eigenschaften neuer Dateiformate und Datenspeicher finden Sie unter [Erweitern des Indexes](-search-3x-wds-extidx-overview.md).
-   Informationen zu Übersichten des Katalog-Managers und des Katalog-Such-Managers (CSM) finden [Sie unter Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).

Konzeptionelle Hintergrundinformationen zu Dateitypen und Handlern finden Sie in den folgenden Themen:

-   Informationen zum Erweitern der Shell mit Dateityp Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md).
-   Konzeptionelle Informationen zu Filter Handlern finden Sie unter [entwickeln von Filter Handlern](-search-ifilter-conceptual.md).
-   Weitere Informationen zum Erstellen von Handlern finden [Sie unter Einführung in Dateizuordnungen](../shell/fa-intro.md), [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md), [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md), [Kontextmenü](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))und [Vorschau Handler](../shell/preview-handlers.md).

Hintergrundinformationen zu verwandten Technologien und zum Implementieren eines Datenspeicher finden Sie in den folgenden Themen:

-   Windows Search-Protokollhandler verwenden Designspezifikationen ähnlich wie SharePoint Server, und Sie können häufig austauschbar verwendet werden. Weitere Informationen finden Sie im [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).
-   In Windows 7 und höher unterstützen SharePoint Search Server 2008 und MOSS 2007 SP2 auch die Verbund Suche. Weitere Informationen über die Verbund Suche und die Search Server 2008-Bereitstellung mit Office SharePoint Server 2007 finden Sie unter [Verbund Search \[ Search Server 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Codebeispiele finden Sie auf den folgenden Portalseiten:

-   Informationen zu Such Codebeispielen finden Sie unter [Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Shell-Codebeispiele finden Sie unter [shellsdk-Beispiele](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).

 

 
