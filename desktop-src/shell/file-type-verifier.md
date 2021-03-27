---
description: Der Dateityp Verifier ist ein Tool, mit dem unabhängige Softwarehersteller überprüfen können, ob Ihre eindeutigen Dateitypen ordnungsgemäß implementiert werden.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Dateityp Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864948"
---
# <a name="file-type-verifier"></a><span data-ttu-id="6748d-103">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="6748d-103">File Type Verifier</span></span>

<span data-ttu-id="6748d-104">Der Dateityp Verifier ist ein Tool, mit dem unabhängige Softwarehersteller überprüfen können, ob Ihre eindeutigen Dateitypen ordnungsgemäß implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6748d-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="6748d-105">Hochwertige Implementierungen ihrer Dateityp Handler sind für eine gute Benutzer Leistung von entscheidender Bedeutung, da Benutzer in Windows-Explorer auf vielerlei Weise mit Ihrem Dateiformat interagieren.</span><span class="sxs-lookup"><span data-stu-id="6748d-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="6748d-106">Benutzer können voll Text suchen durchführen, nach benutzerdefinierten Metadaten sortieren oder umfassende Miniaturansichten und Vorschau Versionen Ihres Datei Formats anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6748d-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="6748d-107">Anweisungen zur Verwendung der Dateityp Überprüfung finden Sie unter [Verwenden des Dateityp-verifizierers](how-to-use-the-file-type-verifier.md).</span><span class="sxs-lookup"><span data-stu-id="6748d-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="6748d-108">Informationen zum Dateityp-Verifier-Tool</span><span class="sxs-lookup"><span data-stu-id="6748d-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="6748d-109">Der Dateityp Verifier ist ein Programm, das als Teil des [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6748d-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6748d-110">Es wurde entwickelt, um Entwicklern zu helfen, die benutzerdefinierte Windows- [Dateitypen](fa-file-types.md) erstellen, um potenzielle Probleme mit ihren Dateitypen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="6748d-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="6748d-111">Obwohl der Dateityp Verifier nur unter Windows 7 und höher ausgeführt wird, gelten die Regeln, die vom Dateityp Verifier erzwungen werden, für alle Windows-Versionen, auf denen die von ihm überprüfen Features verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6748d-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="6748d-112">Die Dateityp Überprüfung führt verschiedene Tests für den Dateityp aus, um sicherzustellen, dass Sie ordnungsgemäß registriert ist, und stellt die entsprechenden [Dateityp Handler](fa-file-extensions.md) bereit, um den Dateityp in Windows-Explorer ordnungsgemäß anzuzeigen, und wenn dies der Fall ist, wird die Indizierung des Datei Inhalts unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6748d-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="6748d-113">Der Dateityp Verifier testet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6748d-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="6748d-114">Vorschau Handler</span><span class="sxs-lookup"><span data-stu-id="6748d-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="6748d-115">Miniatur Ansichts Handler</span><span class="sxs-lookup"><span data-stu-id="6748d-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="6748d-116">Eigenschaften Handler</span><span class="sxs-lookup"><span data-stu-id="6748d-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="6748d-117">Verb Handler</span><span class="sxs-lookup"><span data-stu-id="6748d-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="6748d-118">Filter (IFilter)</span><span class="sxs-lookup"><span data-stu-id="6748d-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="6748d-119">Kind-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="6748d-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="6748d-120">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="6748d-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="6748d-121">Wichtige Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6748d-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="6748d-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6748d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6748d-123">Verwenden des Dateityp-verifizierers</span><span class="sxs-lookup"><span data-stu-id="6748d-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="6748d-124">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="6748d-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="6748d-125">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="6748d-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="6748d-126">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="6748d-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="6748d-127">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="6748d-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="6748d-128">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="6748d-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="6748d-129">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="6748d-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="6748d-130">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="6748d-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="6748d-131">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="6748d-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
