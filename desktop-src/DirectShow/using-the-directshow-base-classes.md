---
description: Verwenden der DirectShow-Basisklassen
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Verwenden der DirectShow-Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216783"
---
# <a name="using-the-directshow-base-classes"></a><span data-ttu-id="44390-103">Verwenden der DirectShow-Basisklassen</span><span class="sxs-lookup"><span data-stu-id="44390-103">Using the DirectShow Base Classes</span></span>

<span data-ttu-id="44390-104">Wenn Sie die Basisklassen in DirectShow verwenden möchten, müssen Sie die Basisklassen Bibliothek erstellen und verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="44390-104">To use the base classes in DirectShow, you must build and link the base class library.</span></span>

<span data-ttu-id="44390-105">Die Basisklassen Bibliothek wird als SDK-Beispiel im Microsoft Windows Software Development Kit (SDK) () bereitgestellt <https://go.microsoft.com/fwlink/p/?linkid=62332> .</span><span class="sxs-lookup"><span data-stu-id="44390-105">The base class library is provided as a SDK sample in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span> <span data-ttu-id="44390-106">Der genaue Speicherort hängt von der Version des SDK ab, das Sie installiert haben, aber der relative Pfad lautet:</span><span class="sxs-lookup"><span data-stu-id="44390-106">The exact location depends on the version of the SDK that you have installed, but the relative path is:</span></span>

<span data-ttu-id="44390-107">*(SDK Samples root)* \\ DirectShow- \\ baseclasses</span><span class="sxs-lookup"><span data-stu-id="44390-107">*(SDK samples root)*\\DirectShow\\BaseClasses</span></span>

<span data-ttu-id="44390-108">Header: Streams. h</span><span class="sxs-lookup"><span data-stu-id="44390-108">Header: Streams.h</span></span>

<span data-ttu-id="44390-109">Library: das Beispiel erstellt die Verkaufs-und Debugversionen der Bibliothek:</span><span class="sxs-lookup"><span data-stu-id="44390-109">Library: The sample builds retail and debug versions of the library:</span></span>

-   <span data-ttu-id="44390-110">Verkaufsversion: "mbase. lib"</span><span class="sxs-lookup"><span data-stu-id="44390-110">Retail version: Strmbase.lib</span></span>
-   <span data-ttu-id="44390-111">Debugversion: "straumbasd. lib".</span><span class="sxs-lookup"><span data-stu-id="44390-111">Debug version: Strmbasd.lib.</span></span>

<span data-ttu-id="44390-112">Weitere Informationen zum Einrichten der Buildumgebung finden Sie unter [Einrichten der Buildumgebung](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="44390-112">For more information on setting up your build environment, see [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

## <a name="preprocessor-symbols"></a><span data-ttu-id="44390-113">Präprozessorsymbole</span><span class="sxs-lookup"><span data-stu-id="44390-113">Preprocessor Symbols</span></span>

<span data-ttu-id="44390-114">Wenn Sie die Header Datei Streams. h einschließen, haben die folgenden Präprozessorsymbole eine besondere Bedeutung:</span><span class="sxs-lookup"><span data-stu-id="44390-114">When you include the header file Streams.h, the following preprocessor symbols have special meaning:</span></span>

-   <span data-ttu-id="44390-115">Perf: reserviert.</span><span class="sxs-lookup"><span data-stu-id="44390-115">PERF: Reserved.</span></span> <span data-ttu-id="44390-116">Verwenden Sie dieses Präprozessorsymbol nicht.</span><span class="sxs-lookup"><span data-stu-id="44390-116">Do not use this preprocessor symbol.</span></span>
-   <span data-ttu-id="44390-117">Vfwrobust: aktiviert die Zeiger Validierung im Einzelhandel.</span><span class="sxs-lookup"><span data-stu-id="44390-117">VFWROBUST: Enables pointer validation in retail.</span></span> <span data-ttu-id="44390-118">Weitere Informationen finden Sie unter [Zeiger Validierungs Makros](pointer-validation-macros.md).</span><span class="sxs-lookup"><span data-stu-id="44390-118">For more information, see [Pointer Validation Macros](pointer-validation-macros.md).</span></span> <span data-ttu-id="44390-119">In Debugbuilds ist es nicht notwendig, vfwrobust zu definieren.</span><span class="sxs-lookup"><span data-stu-id="44390-119">In debug builds, it is not necessary to define VFWROBUST.</span></span>

> [!Note]  
> <span data-ttu-id="44390-120">In Windows Vista und höher sind die Zeiger Validierungs Makros leer.</span><span class="sxs-lookup"><span data-stu-id="44390-120">In Windows Vista and later, the pointer validation macros are empty.</span></span>

 

 

 



