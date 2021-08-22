---
description: Dieser Abschnitt enthält grundlegende Informationen, die für die Implementierung, Erweiterung und das Testen von Protokollhandlern erforderlich sind.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Entwickeln von Protokollhandlern für die Windows Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ef01d36e565471756ee9d6680833401054a6e29b9c570dad7852d316797067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597830"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>Entwickeln von Protokollhandlern für die Windows Suche

Dieser Abschnitt enthält grundlegende Informationen, die für die Implementierung, Erweiterung und das Testen von Protokollhandlern erforderlich sind.

-   [Grundlegendes zu Protokollhandlern](-search-3x-wds-extidx-prot-implementing.md)
-   [Benachrichtigen des Änderungsindexes](-search-3x-wds-notifyingofchanges.md)
-   [Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
-   [Codebeispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
-   [Installieren und Registrieren von Protokollhandlern](-search-3x-wds-ph-install-registration.md)
-   [Erstellen eines Suchconnectors für einen Protokollhandler](-search-3x-wds-ph-search-connector.md)
-   [Debuggen von Protokollhandlern](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>Weitere Ressourcen

Konzeptionelle Hintergrundinformationen zur Indizierung finden Sie in den folgenden Themen:

-   Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess.](-search-indexing-process-overview.md)
-   Informationen zum Erweitern Windows Search zum Indizierung des Inhalts und der Eigenschaften neuer Dateiformate und Datenspeicher finden Sie unter [Erweitern des Indexes.](-search-3x-wds-extidx-overview.md)
-   Übersichten über den Katalog-Manager und den Katalogsuche-Manager (Catalog Search Manager, CSM) finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md).

Konzeptionelle Hintergrundinformationen zu Dateitypen und Handlern finden Sie in den folgenden Themen:

-   Informationen zum Erweitern der Shell mit Dateityphandlern finden Sie unter [Erstellen von Shellerweiterungshandlern.](../shell/handlers.md)
-   Konzeptionelle Informationen zu Filterhandlern finden Sie unter [Entwickeln von Filterhandlern.](-search-ifilter-conceptual.md)
-   Informationen zum Erstellen von Handlern finden Sie unter [Einführung in Dateizuordnungen,](../shell/fa-intro.md) [Registrieren von Shellerweiterungen,](../shell/reg-shell-exts.md) [Erstellen von Shellerweiterungshandlern,](../shell/handlers.md) [Kontextmenü](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))und [Vorschauhandlern.](../shell/preview-handlers.md)

Hintergrundinformationen zu verwandten Technologien und zur Implementierung eines Datenspeichers finden Sie in den folgenden Themen:

-   Windows Suchprotokollhandler verwenden Entwurfsspezifikationen, die SharePoint Server ähneln, und sie können häufig austauschbar verwendet werden. Weitere Informationen finden Sie unter [SharePoint Server Developer Center.](https://developer.microsoft.com/office/docs)
-   In Windows 7 und höher unterstützen SharePoint Search Server 2008 und MOSS 2007 SP2 auch die Verbundsuche. Weitere Informationen zur Verbundsuche und zur Bereitstellung von Search Server 2008 mit Office SharePoint Server 2007 finden Sie unter [ \[ Suchserver \] 2008 im Verbund.](/previous-versions/office/bb931109(v=office.14))
-   Informationen zum Erstellen eines Shell-Datenspeichers finden Sie unter [Implementieren der grundlegenden Ordnerobjektschnittstellen.](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))

Codebeispiele finden Sie auf den folgenden Portalseiten:

-   Codebeispiele für die Suche finden Sie unter [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Shell-Codebeispiele finden Sie unter [Shell SDK-Beispiele.](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85))

 

 
