---
description: Mit Windows Vista werden neue Speicher Szenarien und ein neuer Namespace für Benutzerprofile eingeführt.
title: Bekannte Ordner
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980241"
---
# <a name="known-folders"></a><span data-ttu-id="a99e8-103">Bekannte Ordner</span><span class="sxs-lookup"><span data-stu-id="a99e8-103">Known Folders</span></span>

<span data-ttu-id="a99e8-104">Mit Windows Vista werden neue Speicher Szenarien und ein neuer Namespace für Benutzerprofile eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a99e8-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="a99e8-105">Um diese neuen Faktoren zu beheben, wurde das ältere System, das über einen [**CSIDL**](csidl.md) -Wert auf Standardordner verweist, ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a99e8-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="a99e8-106">Ab Windows Vista wird auf diese Ordner durch einen neuen Satz von GUID-Werten verwiesen, die als bekannte Ordner-IDs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a99e8-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="a99e8-107">Das bekannte Ordnersystem bietet folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="a99e8-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="a99e8-108">Unabhängige Softwarehersteller (ISVs) können den Satz bekannter Ordner-IDs mit eigenen Erweiterungen erweitern.</span><span class="sxs-lookup"><span data-stu-id="a99e8-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="a99e8-109">Sie können Ordner definieren, Ihnen IDs zuordnen und Sie beim System registrieren.</span><span class="sxs-lookup"><span data-stu-id="a99e8-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="a99e8-110">CSIDL-Werte konnten nicht erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="a99e8-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="a99e8-111">Alle bekannten Ordner auf einem System können aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="a99e8-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="a99e8-112">Diese Funktionalität für CSIDL-Werte wurde von keiner API bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a99e8-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="a99e8-113">Weitere Informationen finden Sie unter [**iknownfoldermanager:: getfolderids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .</span><span class="sxs-lookup"><span data-stu-id="a99e8-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="a99e8-114">Ein bekannter Ordner, der von einem ISV hinzugefügt wird, kann benutzerdefinierte Eigenschaften hinzufügen, mit denen er den Zweck und die beabsichtigte Verwendung erläutern kann.</span><span class="sxs-lookup"><span data-stu-id="a99e8-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="a99e8-115">Viele bekannte Ordner können an neue Speicherorte umgeleitet werden, einschließlich Netzwerkadressen.</span><span class="sxs-lookup"><span data-stu-id="a99e8-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="a99e8-116">Unter dem CSIDL-System konnte nur der Ordner " **Eigene Dokumente** " umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a99e8-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="a99e8-117">Bekannte Ordner können benutzerdefinierte Handler für die Verwendung während der Erstellung oder Löschung enthalten.</span><span class="sxs-lookup"><span data-stu-id="a99e8-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="a99e8-118">Das CSIDL-System und APIs, die CSIDL-Werte verwenden, werden weiterhin aus Kompatibilitätsgründen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a99e8-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="a99e8-119">Es wird jedoch nicht empfohlen, diese in einer neuen Entwicklung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a99e8-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="a99e8-120">In den folgenden Themen werden die Besonderheiten des Systems "bekannte Ordner" erläutert.</span><span class="sxs-lookup"><span data-stu-id="a99e8-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="a99e8-121">Arbeiten mit bekannten Ordnern in Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a99e8-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="a99e8-122">Erweitern bekannter Ordner mit benutzerdefinierten Ordnern</span><span class="sxs-lookup"><span data-stu-id="a99e8-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="a99e8-123">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="a99e8-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="a99e8-124">Auf den folgenden Referenzseiten werden die Funktionen von Win32-Funktionen für bekannte Ordner erläutert, die zum Abrufen des Speicher Orts bekannter Ordner oder zum Umleiten an einen neuen Speicherort verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a99e8-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="a99e8-125">Diese Funktionen ersetzen ältere Win32-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a99e8-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="a99e8-126">Die neuen Funktionen werden bereitgestellt, um den alten Funktionen ein entsprechendes Verhalten zu bieten, aber jede neue Funktion wird auch durch eine Component Object Model (com)-API dupliziert.</span><span class="sxs-lookup"><span data-stu-id="a99e8-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="a99e8-127">Neue Funktion</span><span class="sxs-lookup"><span data-stu-id="a99e8-127">New Function</span></span>                                             | <span data-ttu-id="a99e8-128">Arbeits</span><span class="sxs-lookup"><span data-stu-id="a99e8-128">Replaces</span></span>                                           | <span data-ttu-id="a99e8-129">COM-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="a99e8-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="a99e8-130">**Shgetknownfolderpath**</span><span class="sxs-lookup"><span data-stu-id="a99e8-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="a99e8-131">**SHGetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="a99e8-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="a99e8-132">**Iknownfolder:: getpath**</span><span class="sxs-lookup"><span data-stu-id="a99e8-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="a99e8-133">**Shgetknownfolderidlist**</span><span class="sxs-lookup"><span data-stu-id="a99e8-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="a99e8-134">**Shgetfolderlocation**</span><span class="sxs-lookup"><span data-stu-id="a99e8-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="a99e8-135">**Iknownfolder:: getidlist**</span><span class="sxs-lookup"><span data-stu-id="a99e8-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="a99e8-136">**Shsetknownfolderpath**</span><span class="sxs-lookup"><span data-stu-id="a99e8-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="a99e8-137">**Shsetfolderpath**</span><span class="sxs-lookup"><span data-stu-id="a99e8-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="a99e8-138">**Iknownfolder:: setpath**</span><span class="sxs-lookup"><span data-stu-id="a99e8-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="a99e8-139">Die folgenden Referenzseiten erläutern die COM-APIs für bekannte Ordner, die die gesamte Funktionalität der oben aufgeführten Win32-APIs bereitstellen, sowie die Möglichkeit, alle bekannten Ordner aufzulisten, auf bekannte Ordnereigenschaften zuzugreifen und den Standardsatz bekannter Ordner zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a99e8-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="a99e8-140">**Iknownfolder**</span><span class="sxs-lookup"><span data-stu-id="a99e8-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="a99e8-141">**Iknownfoldermanager**</span><span class="sxs-lookup"><span data-stu-id="a99e8-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="a99e8-142">Im Windows Software Development Kit (SDK) ist ein C++-Beispiel enthalten, das die APIs bekannter Ordner veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a99e8-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a99e8-143">Nachdem Sie die Windows SDK auf Ihrem Computer installiert haben, finden Sie das Beispiel unter% Program Files% \\ Microsoft \\ \\ sdgs Windows v 6.0 \\ Samples \\ WinUI \\ Shell \\ appplatform \\ KnownFolders.</span><span class="sxs-lookup"><span data-stu-id="a99e8-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a99e8-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a99e8-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a99e8-145">[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a99e8-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
