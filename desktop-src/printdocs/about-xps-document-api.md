---
description: Die XPS-Dokument-API implementiert das XPS-Objektmodell und ermöglicht Entwicklern das Erstellen eines XPS-OM, das Bearbeiten von XPS-Dokument Inhalten in systemeigenen Windows \\ \\ -Programmen und das Speichern des XPS-Maps in einer Datei oder einem Stream als XPS-Dokument.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Informationen zur XPS-Dokument-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351010"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="4a867-103">Informationen zur XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="4a867-103">About XPS Document API</span></span>

<span data-ttu-id="4a867-104">Die [XPS-Dokument-API](documents-xps.md) implementiert das XPS-Objektmodell und ermöglicht Entwicklern das Erstellen eines XPS-OM, das Bearbeiten von XPS-Dokument Inhalten in systemeigenen Windows \\ \\ -Programmen und das Speichern des XPS-Maps in einer Datei oder einem Stream als XPS-Dokument.</span><span class="sxs-lookup"><span data-stu-id="4a867-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="4a867-105">Entwickler von XPSDrv-Filter Pipeline Modulen können auch die XPS-Dokument-API verwenden, um XPS-Dokumentinhalte in einem XPSDrv-Druckertreiber Filter zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a867-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="4a867-106">Übersicht über XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="4a867-106">XPS Document API Overview</span></span>

<span data-ttu-id="4a867-107">Das XPS-Objektmodell ist das Informationsmodell eines XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4a867-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="4a867-108">Das Informationsmodell des XPS-Dokuments ist von dem Markup Modell getrennt, das in den Dokument Teilen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a867-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="4a867-109">Das XPS-Objektmodell beschreibt die Organisation der internen Komponenten, aus denen ein XPS-Dokument besteht, und das Markup Modell beschreibt den Inhalt dieser Komponenten.</span><span class="sxs-lookup"><span data-stu-id="4a867-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="4a867-110">In einem Programm wird das XPS-Objektmodell als XPS-OM instanziiert.</span><span class="sxs-lookup"><span data-stu-id="4a867-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="4a867-111">Beim XPS-OM handelt es sich im Wesentlichen um eine in-Memory-Version des Inhalts eines XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4a867-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="4a867-112">Obwohl es in der logischen Organisation zu einem XPS-Dokument kommt, wird ein XPS-OM-Objekt erst als XPS-Dokument betrachtet, wenn es in eine Datei oder einen Stream serialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a867-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="4a867-113">Die genaue Struktur des Markups ist für das XPS-om nicht verfügbar, wenn ein XPS-Dokument von einem Markup zu einem XPS-OM deserialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a867-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="4a867-114">Beispielsweise wird, unabhängig davon, ob die Eigenschaft als Element oder Attribut im Markup dargestellt wurde, der Eigenschafts Wert eines Dokument Objekts auf genau die gleiche Weise vom XPS-OM dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4a867-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="4a867-115">Die [XPS-Dokument-API](documents-xps.md) kann in die folgenden Kategorien unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="4a867-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="4a867-116">XPS-OM-trunk Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4a867-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="4a867-117">Die trunk Schnittstellen ermöglichen den Zugriff auf die Komponenten der obersten Ebene der XPS-Dokumentstruktur.</span><span class="sxs-lookup"><span data-stu-id="4a867-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="4a867-118">Diese Schnittstellen bieten außerdem die Möglichkeit, ein XPS-OM zu serialisieren und ein XPS-Dokument zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="4a867-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="4a867-119">XPS-Schnittstellen für Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4a867-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="4a867-120">Die Seiten Schnittstellen ermöglichen den Zugriff auf den Inhalt einer Seite in einem XPS-Dokument.</span><span class="sxs-lookup"><span data-stu-id="4a867-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="4a867-121">Die Schnittstellen, die den Inhalt der Seite beschreiben, sind auch in den Seiten Schnittstellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a867-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="4a867-122">Digitale XPS-OM-Signaturen</span><span class="sxs-lookup"><span data-stu-id="4a867-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="4a867-123">Das XPS-OM unterstützt digitale Signaturen.</span><span class="sxs-lookup"><span data-stu-id="4a867-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="4a867-124">Sie können jedoch direkt auf digitale Signaturen in einem XPS-Dokument zugreifen, ohne ein XPS-OM erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4a867-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="4a867-125">Weitere Informationen zum Zugreifen auf XPS Digital Signaturen ohne XPS-OM finden Sie unter [XPS Digital Signature API](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="4a867-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="4a867-126">Schnittstellen für XPS-OM-Druck Tickets</span><span class="sxs-lookup"><span data-stu-id="4a867-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="4a867-127">XPS-Dokumente unterstützen Druck Tickets auf Paket-(Auftrags-), Dokument-und Seitenebene.</span><span class="sxs-lookup"><span data-stu-id="4a867-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="4a867-128">Druck Tickets enthalten Informationen zum Formatieren von Dokument Inhalten zum Drucken oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a867-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a867-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a867-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4a867-130">**In diesem Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="4a867-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="4a867-131">XPS-OM-trunk Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4a867-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4a867-132">XPS-Schnittstellen für Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4a867-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4a867-133">Digitale XPS-OM-Signaturen</span><span class="sxs-lookup"><span data-stu-id="4a867-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="4a867-134">Schnittstellen für XPS-OM-Druck Tickets</span><span class="sxs-lookup"><span data-stu-id="4a867-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="4a867-135">**Weitere verwandte Themen**</span><span class="sxs-lookup"><span data-stu-id="4a867-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="4a867-136">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="4a867-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="4a867-137">Digitale XPS-OM-Signaturen</span><span class="sxs-lookup"><span data-stu-id="4a867-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="4a867-138">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="4a867-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="4a867-139">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4a867-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



