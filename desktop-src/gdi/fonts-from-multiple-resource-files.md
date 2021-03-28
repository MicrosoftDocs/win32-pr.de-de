---
description: Schriftarten aus mehreren Ressourcen Dateien
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Schriftarten aus mehreren Ressourcen Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2021
ms.locfileid: "104996450"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="a00d2-103">Schriftarten aus mehreren Ressourcen Dateien</span><span class="sxs-lookup"><span data-stu-id="a00d2-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="a00d2-104">In der Regel ist eine Schriftart in einer einzelnen Schriftart Ressourcen Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="a00d2-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="a00d2-105">Die Informationen für einige Schriftarten sind jedoch auf mehrere Dateien verteilt.</span><span class="sxs-lookup"><span data-stu-id="a00d2-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="a00d2-106">Beispielsweise sind für Typ 1 mehrere Master Schriftarten zwei Dateien erforderlich:</span><span class="sxs-lookup"><span data-stu-id="a00d2-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="a00d2-107">PFM für die Schriftart Metrik</span><span class="sxs-lookup"><span data-stu-id="a00d2-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="a00d2-108">PFB für Schriftart Bits</span><span class="sxs-lookup"><span data-stu-id="a00d2-108">.pfb for the font bits</span></span>

<span data-ttu-id="a00d2-109">Um dem System eine Schriftart aus mehreren Dateien hinzuzufügen, verwenden Sie die Funktionen [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) oder [**addfontresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) .</span><span class="sxs-lookup"><span data-stu-id="a00d2-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="a00d2-110">Der *lpszfilename* -Parameter in diesen Funktionen muss auf eine Zeichenfolge verweisen, die die Dateinamen enthält, die durch einen senkrechten Strich oder eine Pipe () getrennt sind \| .</span><span class="sxs-lookup"><span data-stu-id="a00d2-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="a00d2-111">Um z. b. abcxxxxx. PFM und abcxxxxx. PFB für eine Schriftart vom Typ 1 anzugeben, verwenden Sie die Zeichenfolge "abcxxxxx. PFM \| abcxxxxx. PFB".</span><span class="sxs-lookup"><span data-stu-id="a00d2-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="a00d2-112">[**Addfontresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) unterscheidet sich von [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) dahin, dass die Anwendung, die **addfontresourceex** aufruft, die Schriftart als privat oder nicht Aufzähl Bar angeben kann.</span><span class="sxs-lookup"><span data-stu-id="a00d2-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="a00d2-113">Um eine Schriftart aus einem Speicher Image hinzuzufügen, verwenden Sie [**addfontmemresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="a00d2-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="a00d2-114">Dadurch kann eine Anwendung eine Schriftart verwenden, die in ein Dokument oder eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="a00d2-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="a00d2-115">Um eine Schriftart zu entfernen, die aus mehreren Ressourcen Dateien stammt, müssen Sie [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) oder [**removefontresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)aufrufen, je nachdem, welche Funktion zum Hinzufügen der Schriftart verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a00d2-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="a00d2-116">Sie müssen die gleichen Flags angeben, die zum Hinzufügen der Schriftart verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a00d2-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="a00d2-117">Verwenden Sie [**removefontmemresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex), um eine Schriftart zu entfernen, die aus einem Speicher Abbild hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a00d2-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="a00d2-118">Die Verwendung einer Schriftart, die aus mehreren Schriftart Ressourcen Dateien stammt, ist identisch mit der Verwendung einer Schriftart aus einer einzelnen Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="a00d2-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
