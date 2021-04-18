---
title: LibMain. CPP
description: In der Beispiel Anbieter Komponente ist ein Codebeispiel für den Standard-DLL-Einstiegspunkt für Adssmp.dll in LibMain. cpp. In der folgenden Tabelle sind die unterstützten Routinen aufgeführt.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340810"
---
# <a name="libmaincpp"></a><span data-ttu-id="a6ac1-104">LibMain. CPP</span><span class="sxs-lookup"><span data-stu-id="a6ac1-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="a6ac1-105">In der Beispiel Anbieter Komponente ist ein Codebeispiel für den Standard-DLL-Einstiegspunkt für Adssmp.dll in LibMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="a6ac1-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="a6ac1-106">In der folgenden Tabelle sind die unterstützten Routinen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6ac1-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="a6ac1-107">Element</span><span class="sxs-lookup"><span data-stu-id="a6ac1-107">Item</span></span>                                  | <span data-ttu-id="a6ac1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6ac1-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a6ac1-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="a6ac1-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="a6ac1-110">Der Standard-DLL-Einstiegspunkt für die Suche nach klassenfac</span><span class="sxs-lookup"><span data-stu-id="a6ac1-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="a6ac1-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="a6ac1-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="a6ac1-112">Standard-DLL-Einstiegspunkt, um zu bestimmen, ob die DLL entladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6ac1-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="a6ac1-113">**LibMain**</span><span class="sxs-lookup"><span data-stu-id="a6ac1-113">**LibMain**</span></span><br/>                | <span data-ttu-id="a6ac1-114">Einstiegspunkt für die Initialisierung der Standard-dll.</span><span class="sxs-lookup"><span data-stu-id="a6ac1-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="a6ac1-115">**Iscompatibleoleversion**</span><span class="sxs-lookup"><span data-stu-id="a6ac1-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="a6ac1-116">Überprüfen Sie die Kompatibilität mit der OLE-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="a6ac1-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="a6ac1-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="a6ac1-117">**DllMain**</span></span><br/>                | <span data-ttu-id="a6ac1-118">Einstiegspunkt für die meisten Versionen von Windows 2000 oder Windows NT.</span><span class="sxs-lookup"><span data-stu-id="a6ac1-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





