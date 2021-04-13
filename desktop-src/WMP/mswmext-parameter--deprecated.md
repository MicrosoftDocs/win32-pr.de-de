---
title: Mswap-Parameter (veraltet)
description: Mswap-Parameter (veraltet)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Media Metafiles, mswap-Parameter
- Metafiles, mswap-Parameter
- Mswap-Parameter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389962"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="7dd53-106">Mswap-Parameter (veraltet)</span><span class="sxs-lookup"><span data-stu-id="7dd53-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="7dd53-107">Der *mswap* -Parameter gibt einem Client Programm das Format einer referenzierten Datei an.</span><span class="sxs-lookup"><span data-stu-id="7dd53-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="7dd53-108">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="7dd53-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="7dd53-109">**Beispiel Code**</span><span class="sxs-lookup"><span data-stu-id="7dd53-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="7dd53-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7dd53-110">Remarks</span></span>

<span data-ttu-id="7dd53-111">Client Programme verwenden manchmal eine Dateinamenerweiterung oder einen MIME-Typ, um zu bestimmen, ob eine Mediendatei als Stream gerenbt werden soll, ob die Datei nach einem vollständigen Download gerenbt werden soll oder ob die Datei überhaupt nicht gerenbt wird.</span><span class="sxs-lookup"><span data-stu-id="7dd53-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="7dd53-112">Wenn ein Client Programm nicht bestimmen kann, wie eine Mediendatei auf der Grundlage der Dateinamenerweiterung oder des MIME-Typs behandelt werden soll, kann er bestimmen, wie die Datei behandelt werden soll, indem der *mswap* -Parameter überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="7dd53-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="7dd53-113">Beispielsweise kann der Client die Datei so behandeln, als hätte Sie eine Erweiterung, die gleich dem Wert des *mswap* -Parameters ist.</span><span class="sxs-lookup"><span data-stu-id="7dd53-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="7dd53-114">Weitere Informationen zu MIME-Typen und Dateinamen Erweiterungen finden Sie unter [Dateinamen Erweiterungen](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="7dd53-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="7dd53-115">Weitere Informationen zum *mswap* -Parameter finden Sie im Artikel [236895](https://support.microsoft.com/kb/236895) in der Microsoft Knowledge Base.</span><span class="sxs-lookup"><span data-stu-id="7dd53-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dd53-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7dd53-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dd53-117">**Frühere Versionen von Windows Media-Metadatendateien (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="7dd53-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




