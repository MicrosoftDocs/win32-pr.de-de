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
# <a name="developing-protocol-handlers-for-windows-search"></a><span data-ttu-id="3ee7c-103">Entwickeln von Protokoll Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="3ee7c-103">Developing Protocol Handlers for Windows Search</span></span>

<span data-ttu-id="3ee7c-104">Dieser Abschnitt enthält konzeptionelle Informationen, die für die Implementierung, Erweiterung und das Testen von Protokoll Handlern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3ee7c-104">This section provides conceptual information necessary for the implementation, extension and testing of protocol handlers.</span></span>

-   [<span data-ttu-id="3ee7c-105">Grundlegendes zu Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="3ee7c-105">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
-   [<span data-ttu-id="3ee7c-106">Benachrichtigen des Index von Änderungen</span><span class="sxs-lookup"><span data-stu-id="3ee7c-106">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
-   [<span data-ttu-id="3ee7c-107">Hinzufügen von Symbolen und Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="3ee7c-107">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
-   [<span data-ttu-id="3ee7c-108">Code Beispiel: Shellerweiterungen für Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="3ee7c-108">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
-   [<span data-ttu-id="3ee7c-109">Installieren und Registrieren von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="3ee7c-109">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
-   [<span data-ttu-id="3ee7c-110">Erstellen eines Suchconnector für einen Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="3ee7c-110">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
-   [<span data-ttu-id="3ee7c-111">Debuggen von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="3ee7c-111">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a><span data-ttu-id="3ee7c-112">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3ee7c-112">Additional Resources</span></span>

<span data-ttu-id="3ee7c-113">Konzeptionelle Hintergrundinformationen zur Indizierung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="3ee7c-113">For conceptual background on indexing, see the following topics:</span></span>

-   <span data-ttu-id="3ee7c-114">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-114">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="3ee7c-115">Informationen zum Erweitern von Windows Search zum Indizieren des Inhalts und der Eigenschaften neuer Dateiformate und Datenspeicher finden Sie unter [Erweitern des Indexes](-search-3x-wds-extidx-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-115">To extend Windows Search to index the contents and properties of new file formats and data stores, see [Extending the Index](-search-3x-wds-extidx-overview.md).</span></span>
-   <span data-ttu-id="3ee7c-116">Informationen zu Übersichten des Katalog-Managers und des Katalog-Such-Managers (CSM) finden [Sie unter Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-116">For overviews of the Catalog Manager and Catalog Search Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

<span data-ttu-id="3ee7c-117">Konzeptionelle Hintergrundinformationen zu Dateitypen und Handlern finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="3ee7c-117">For conceptual background on file types and handlers, see the following topics:</span></span>

-   <span data-ttu-id="3ee7c-118">Informationen zum Erweitern der Shell mit Dateityp Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-118">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](../shell/handlers.md).</span></span>
-   <span data-ttu-id="3ee7c-119">Konzeptionelle Informationen zu Filter Handlern finden Sie unter [entwickeln von Filter Handlern](-search-ifilter-conceptual.md).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-119">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>
-   <span data-ttu-id="3ee7c-120">Weitere Informationen zum Erstellen von Handlern finden [Sie unter Einführung in Dateizuordnungen](../shell/fa-intro.md), [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md), [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md), [Kontextmenü](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))und [Vorschau Handler](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-120">For information about creating handlers, see [Introduction to File Associations](../shell/fa-intro.md), [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [Preview Handlers](../shell/preview-handlers.md).</span></span>

<span data-ttu-id="3ee7c-121">Hintergrundinformationen zu verwandten Technologien und zum Implementieren eines Datenspeicher finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="3ee7c-121">For background on related technologies and on implementing a data store, see the following topics:</span></span>

-   <span data-ttu-id="3ee7c-122">Windows Search-Protokollhandler verwenden Designspezifikationen ähnlich wie SharePoint Server, und Sie können häufig austauschbar verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ee7c-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="3ee7c-123">Weitere Informationen finden Sie im [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-123">For more information, see [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span></span>
-   <span data-ttu-id="3ee7c-124">In Windows 7 und höher unterstützen SharePoint Search Server 2008 und MOSS 2007 SP2 auch die Verbund Suche.</span><span class="sxs-lookup"><span data-stu-id="3ee7c-124">In Windows 7 and later, SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search.</span></span> <span data-ttu-id="3ee7c-125">Weitere Informationen über die Verbund Suche und die Search Server 2008-Bereitstellung mit Office SharePoint Server 2007 finden Sie unter [Verbund Search \[ Search Server 2008 \] ](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-125">For more information about federated search and Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>
-   <span data-ttu-id="3ee7c-126">Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-126">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="3ee7c-127">Codebeispiele finden Sie auf den folgenden Portalseiten:</span><span class="sxs-lookup"><span data-stu-id="3ee7c-127">For code samples, see the following portal pages:</span></span>

-   <span data-ttu-id="3ee7c-128">Informationen zu Such Codebeispielen finden Sie unter [Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-128">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="3ee7c-129">Shell-Codebeispiele finden Sie unter [shellsdk-Beispiele](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ee7c-129">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

 

 
