---
description: Schreiben eines ASF-Header Objekts für eine neue Datei
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Schreiben eines ASF-Header Objekts für eine neue Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366144"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="be692-103">Schreiben eines ASF-Header Objekts für eine neue Datei</span><span class="sxs-lookup"><span data-stu-id="be692-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="be692-104">Das Objekt "ASF ContentInfo" speichert Informationen zu den ASF-Header Objekten für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="be692-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="be692-105">Wenn eine ASF-Datei erstellt oder geändert wird, muss das Header Objekt generiert werden.</span><span class="sxs-lookup"><span data-stu-id="be692-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="be692-106">Hierzu muss die Anwendung das Codierungs Profil des Inhalts für das ContentInfo-Objekt bereitstellen, damit Sie die Merkmale der zu erstellenden Mediendatei kennt.</span><span class="sxs-lookup"><span data-stu-id="be692-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="be692-107">Zum Schreiben einer neuen Datei können Sie das ContentInfo-Objekt für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="be692-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="be692-108">Sammeln von Header Informationen aus dem Profil Objekt der zu erstellenden Datei</span><span class="sxs-lookup"><span data-stu-id="be692-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="be692-109">Auffüllen verschiedener Header Objekte in der von Media Foundation intern verwalteten ASF-Bibliothek,</span><span class="sxs-lookup"><span data-stu-id="be692-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="be692-110">Initialisieren Sie den [ASF Multiplexer](asf-multiplexer.md) für die Erstellung des ASF-Datenpakets.</span><span class="sxs-lookup"><span data-stu-id="be692-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="be692-111">Erstellen Sie das Header Objekt der obersten Ebene im Binärformat, das in eine Datei geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="be692-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="be692-112">Informationen zu Profilen finden Sie unter [ASF-Profil](asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="be692-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="be692-113">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="be692-113">This section contains the following topics:</span></span>



| <span data-ttu-id="be692-114">Thema</span><span class="sxs-lookup"><span data-stu-id="be692-114">Topic</span></span>                                                                                                              | <span data-ttu-id="be692-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be692-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be692-116">Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="be692-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="be692-117">Beschreibt die [**imfasf ContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) -Methode, die das ContentInfo-Objekt mit in einem Profil Objekt gespeicherten Header Informationen initialisiert.</span><span class="sxs-lookup"><span data-stu-id="be692-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="be692-118">Festlegen von Eigenschaften im ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="be692-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="be692-119">Informationen zu verschiedenen Konfigurations Eigenschaften, die für das ContentInfo-Objekt festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="be692-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="be692-120">Erstellen eines neuen ASF-Header Objekts</span><span class="sxs-lookup"><span data-stu-id="be692-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="be692-121">Generieren eines Medien Puffers, der das tatsächliche ASF-Header Objekt der neuen Datei enthält, aus dem ContentInfo-Objekt.</span><span class="sxs-lookup"><span data-stu-id="be692-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="be692-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be692-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be692-123">ASF-ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="be692-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="be692-124">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="be692-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="be692-125">Struktur der ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="be692-125">ASF File Structure</span></span>
</dt> </dl>

 

 



