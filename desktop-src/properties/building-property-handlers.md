---
description: Erfahren Sie, wie Sie einen Eigenschaftenhandler erstellen, der Eigenschaften in und aus einem Dateistream liest und schreibt. Jeder Handler ist einem bestimmten Dateityp zugeordnet.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementieren von Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481835"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="3afc8-104">Implementieren von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="3afc8-104">Implementing Property Handlers</span></span>

<span data-ttu-id="3afc8-105">In Windows Vista und höher wurden Metadaten zu einer zentralen Methode zum Organisieren von Elementen wie Dateien, E-Mails oder Kontakten.</span><span class="sxs-lookup"><span data-stu-id="3afc8-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="3afc8-106">Um ein System zu aktivieren, in dem Elemente basierend auf ihren Metadaten durchsucht werden können und in dem Benutzer diese Metadaten lesen oder schreiben können, hat Windows Vista ein neues Eigenschaftensystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3afc8-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="3afc8-107">Metadaten in diesem System werden durch einen erweiterbaren Satz von Eigenschaften dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3afc8-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="3afc8-108">In diesen Themen wird beschrieben, wie Sie einen Handler erstellen können, der Eigenschaften in und aus einem Dateistream liest und schreibt.</span><span class="sxs-lookup"><span data-stu-id="3afc8-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="3afc8-109">Diese Handler werden als Eigenschaftenhandler bezeichnet und sind jeweils einem bestimmten Dateityp zugeordnet, der durch die Dateierweiterung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3afc8-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="3afc8-110">In den folgenden Themen werden die Anforderungen und Strategien zum Definieren von Eigenschaften und Eigenschaftenhandlern behandelt.</span><span class="sxs-lookup"><span data-stu-id="3afc8-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="3afc8-111">Grundlegendes zu Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="3afc8-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="3afc8-112">Verwenden von Kind-Namen</span><span class="sxs-lookup"><span data-stu-id="3afc8-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="3afc8-113">Verwenden von Eigenschaftenlisten</span><span class="sxs-lookup"><span data-stu-id="3afc8-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="3afc8-114">Initialisieren von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="3afc8-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="3afc8-115">Registrieren und Verteilen von Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="3afc8-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="3afc8-116">Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern</span><span class="sxs-lookup"><span data-stu-id="3afc8-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="3afc8-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3afc8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3afc8-118">Erstellen von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3afc8-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="3afc8-119">Schema der Eigenschaftenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="3afc8-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
