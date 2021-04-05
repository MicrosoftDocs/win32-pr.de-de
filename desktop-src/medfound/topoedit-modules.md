---
description: Topoedit-Module
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Topoedit-Module
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042043"
---
# <a name="topoedit-modules"></a><span data-ttu-id="1ac8c-103">Topoedit-Module</span><span class="sxs-lookup"><span data-stu-id="1ac8c-103">TopoEdit Modules</span></span>

<span data-ttu-id="1ac8c-104">Das Tool topoedit wird mit dem Windows SDK für Windows Server 2008 und höher bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1ac8c-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="1ac8c-105">Das Tool erfordert Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="1ac8c-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="1ac8c-106">Die topoedit-Module befinden sich im Ordner "bin" des SDK.</span><span class="sxs-lookup"><span data-stu-id="1ac8c-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="1ac8c-107">Diese Module sind:</span><span class="sxs-lookup"><span data-stu-id="1ac8c-107">These modules are:</span></span>

-   <span data-ttu-id="1ac8c-108">TopoEdit.exe – ausführbare Datei der Anwendung</span><span class="sxs-lookup"><span data-stu-id="1ac8c-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="1ac8c-109">TEDUTIL.dll –-Erweiterungs-DLL</span><span class="sxs-lookup"><span data-stu-id="1ac8c-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="1ac8c-110">Die SDK-Installation registriert die dll.</span><span class="sxs-lookup"><span data-stu-id="1ac8c-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="1ac8c-111">Wenn dies jedoch nicht möglich ist, führen Sie an einer Eingabeaufforderung Folgendes aus.</span><span class="sxs-lookup"><span data-stu-id="1ac8c-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="1ac8c-112">Quellcode für topoedit wird auch als Beispiel in der Windows SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1ac8c-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="1ac8c-113">Sie befindet sich im folgenden Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="1ac8c-113">It is located in the following directory:</span></span>

<span data-ttu-id="1ac8c-114"><samples root>\\Multimedia- \\ Media Foundation \\ topoedit</span><span class="sxs-lookup"><span data-stu-id="1ac8c-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ac8c-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ac8c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac8c-116">Einführung in topoedit</span><span class="sxs-lookup"><span data-stu-id="1ac8c-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="1ac8c-117">Topoedit</span><span class="sxs-lookup"><span data-stu-id="1ac8c-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



