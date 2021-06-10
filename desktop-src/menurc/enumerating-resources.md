---
title: Aufzählen von Ressourcen
description: In diesem Thema werden die Funktionen erläutert, die zum Abrufen von Ressourcenlisten verwendet werden.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910269"
---
# <a name="enumerating-resources"></a><span data-ttu-id="1de34-103">Aufzählen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1de34-103">Enumerating resources</span></span>

<span data-ttu-id="1de34-104">In bestimmten Situationen sollten Sie den Ressourceninhalt eines unbekannten PE-Moduls (Portable Executable) ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1de34-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="1de34-105">Der Windows SDK stellt Ressourcenenumerationsfunktionen bereit, mit denen Ihre Anwendung Listen von Ressourcentypen, Namen und Sprachen in einem angegebenen Modul abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="1de34-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="1de34-106">Die Funktionen [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) und [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) stellen eine Liste der Ressourcentypen im Modul bereit.</span><span class="sxs-lookup"><span data-stu-id="1de34-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="1de34-107">Die Funktionen [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) und [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) geben den Namen jeder Ressource innerhalb eines bestimmten Typs an.</span><span class="sxs-lookup"><span data-stu-id="1de34-107">The [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="1de34-108">Die Funktionen [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) und [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) stellen die Sprache jeder Ressource mit einem bestimmten Namen und Typ bereit.</span><span class="sxs-lookup"><span data-stu-id="1de34-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="1de34-109">Diese Funktionen und die zugehörigen Rückruffunktionen ermöglichen Es Ihrer Anwendung, eine Liste aller Ressourcen in einem Modul zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1de34-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="1de34-110">Dieser Prozess wird unter [Erstellen einer Ressourcenliste](using-resources.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1de34-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="1de34-111">-see-also</span><span class="sxs-lookup"><span data-stu-id="1de34-111">-see-also</span></span>

[<span data-ttu-id="1de34-112">Msistuff.exe Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="1de34-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
