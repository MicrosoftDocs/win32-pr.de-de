---
description: In Windows Vista und höher wurden Metadaten als Methode zum Organisieren von Elementen, z. b. Dateien, e-Mails oder Kontakten, als zentrales Element.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementieren von Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217017"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="3218a-103">Implementieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="3218a-103">Implementing Property Handlers</span></span>

<span data-ttu-id="3218a-104">In Windows Vista und höher wurden Metadaten als Methode zum Organisieren von Elementen, z. b. Dateien, e-Mails oder Kontakten, als zentrales Element.</span><span class="sxs-lookup"><span data-stu-id="3218a-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="3218a-105">Um ein System zu aktivieren, in dem Elemente basierend auf Ihren Metadaten durchsucht werden können und Benutzer diese Metadaten lesen oder schreiben können, wurde in Windows Vista ein neues Eigenschaften System eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3218a-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="3218a-106">Metadaten in diesem System werden durch einen erweiterbaren Satz von Eigenschaften dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3218a-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="3218a-107">In diesen Themen wird beschrieben, wie Sie einen Handler zum Lesen und Schreiben von Eigenschaften in einen und aus einem Dateistream erstellen können.</span><span class="sxs-lookup"><span data-stu-id="3218a-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="3218a-108">Diese Handler werden als Eigenschaften Handler bezeichnet und jeweils einem angegebenen Dateitypen zugeordnet, die durch die Dateinamenerweiterung identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3218a-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="3218a-109">In den folgenden Themen werden die Anforderungen und Strategien erläutert, die beim Definieren von Eigenschaften und Eigenschaften Handlern beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="3218a-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="3218a-110">Grundlegendes zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="3218a-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="3218a-111">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="3218a-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="3218a-112">Verwenden von Eigenschaften Listen</span><span class="sxs-lookup"><span data-stu-id="3218a-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="3218a-113">Initialisieren von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="3218a-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="3218a-114">Registrieren und Verteilen von Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="3218a-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="3218a-115">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern</span><span class="sxs-lookup"><span data-stu-id="3218a-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="3218a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3218a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3218a-117">Erstellen von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3218a-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="3218a-118">Eigenschafts Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="3218a-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
