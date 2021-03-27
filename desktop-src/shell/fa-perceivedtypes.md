---
description: Ein wahrgenommener Typ ist eine Kategorie von Dateitypen, mit der Sie den Dateityp für Windows (und Anwendungen) als Bild, Audiodaten, Dokument oder anderen Typ identifizieren können.
title: Wahrgenommene Typen (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995278"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="687a2-103">Wahrgenommene Typen (die Windows-Shell)</span><span class="sxs-lookup"><span data-stu-id="687a2-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="687a2-104">Ein wahrgenommener Typ ist eine Kategorie von Dateitypen, mit der Sie den Dateityp für Windows (und Anwendungen) als Bild, Audiodaten, Dokument oder anderen Typ identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="687a2-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="687a2-105">Wahrgenommene Typen werden für verschiedene Zwecke verwendet, einschließlich der Bestimmung des Ordner Typs, der dann zum Festlegen der Standard Ansichts Einstellungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="687a2-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="687a2-106">So wird z. b. einem Ordner, der in Dateien mit dem Bild des Typs wahrgenommen ist, ein Standard Ansichtsmodus für Miniaturansichten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="687a2-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="687a2-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="687a2-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="687a2-108">Informationen zu wahrgenommenen Typen</span><span class="sxs-lookup"><span data-stu-id="687a2-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="687a2-109">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="687a2-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="687a2-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="687a2-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="687a2-111">Informationen zu wahrgenommenen Typen</span><span class="sxs-lookup"><span data-stu-id="687a2-111">About Perceived Types</span></span>

<span data-ttu-id="687a2-112">Wahrgenommene Typen, die als "wahrnehmdtype"-Werte definiert sind, ähneln Dateitypen, außer dass Sie auf allgemeine Kategorien von Dateiformat Typen anstatt auf bestimmte Dateitypen verweisen.</span><span class="sxs-lookup"><span data-stu-id="687a2-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="687a2-113">Beispielsweise werden Bild-, Text-, Audiodaten und komprimierte Typen als Typen angesehen.</span><span class="sxs-lookup"><span data-stu-id="687a2-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="687a2-114">Dateitypen (in der Regel öffentliche Dateitypen) kann ein wahr gegebener Typ zugewiesen werden, und Sie sollten immer eine zugewiesen werden, wenn eine geeignete vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="687a2-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="687a2-115">Die Bild Dateitypen BMP, PNG, JPG und GIF sind z. b. auch das wahrgenommene typimage.</span><span class="sxs-lookup"><span data-stu-id="687a2-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="687a2-116">Die standardmäßig erkannten Typen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="687a2-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="687a2-117">Ordner</span><span class="sxs-lookup"><span data-stu-id="687a2-117">Folder</span></span>
-   <span data-ttu-id="687a2-118">Text</span><span class="sxs-lookup"><span data-stu-id="687a2-118">Text</span></span>
-   <span data-ttu-id="687a2-119">Image</span><span class="sxs-lookup"><span data-stu-id="687a2-119">Image</span></span>
-   <span data-ttu-id="687a2-120">Audio</span><span class="sxs-lookup"><span data-stu-id="687a2-120">Audio</span></span>
-   <span data-ttu-id="687a2-121">Video</span><span class="sxs-lookup"><span data-stu-id="687a2-121">Video</span></span>
-   <span data-ttu-id="687a2-122">Compressed</span><span class="sxs-lookup"><span data-stu-id="687a2-122">Compressed</span></span>
-   <span data-ttu-id="687a2-123">Dokument</span><span class="sxs-lookup"><span data-stu-id="687a2-123">Document</span></span>
-   <span data-ttu-id="687a2-124">System</span><span class="sxs-lookup"><span data-stu-id="687a2-124">System</span></span>
-   <span data-ttu-id="687a2-125">Application</span><span class="sxs-lookup"><span data-stu-id="687a2-125">Application</span></span>
-   <span data-ttu-id="687a2-126">GameMedia</span><span class="sxs-lookup"><span data-stu-id="687a2-126">Gamemedia</span></span>
-   <span data-ttu-id="687a2-127">Kontakte</span><span class="sxs-lookup"><span data-stu-id="687a2-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="687a2-128">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="687a2-128">Additional Resources</span></span>

-   <span data-ttu-id="687a2-129">Informationen zum Registrieren von wahrgenommenen Typen finden Sie unter [Anwendungs Registrierung](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="687a2-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="687a2-130">Eine Liste der erkannten Standardtypen finden Sie unter der [**wahrgenommenen**](/windows/win32/api/shtypes/ne-shtypes-perceived) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="687a2-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="687a2-131">Informationen zum Abrufen des wahrgenommenen Datentyps einer Datei anhand ihrer Dateinamenerweiterung finden Sie unter der Funktion " [**assocgetwahrnehmvedtype**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) ".</span><span class="sxs-lookup"><span data-stu-id="687a2-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="687a2-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="687a2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="687a2-133">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="687a2-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="687a2-134">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="687a2-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="687a2-135">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="687a2-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="687a2-136">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="687a2-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="687a2-137">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="687a2-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="687a2-138">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="687a2-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="687a2-139">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="687a2-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="687a2-140">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="687a2-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



