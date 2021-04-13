---
title: WM/GenreID
description: Das WM/GenreID-Attribut enthält einen Genre Bezeichner, der mit dem Inhalt des TCON-Tags in "ID3v2" kompatibel ist.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- WM/GenreID-Windows Media-Format
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389342"
---
# <a name="wmgenreid"></a><span data-ttu-id="d8122-104">WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="d8122-104">WM/GenreID</span></span>

<span data-ttu-id="d8122-105">Das **WM/GenreID-** Attribut enthält einen Genre Bezeichner, der mit dem Inhalt des TCON-Tags in "ID3v2" kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="d8122-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="d8122-106">Dies sollte die Genre-ID in Klammern enthalten, optional gefolgt von einer Optimierung, die das Genre beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d8122-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="d8122-107">Weitere Informationen finden Sie in der Spezifikation "ID3v2".</span><span class="sxs-lookup"><span data-stu-id="d8122-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d8122-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="d8122-108">Global Constant</span></span>

<span data-ttu-id="d8122-109">g \_ wszwmgenreid</span><span class="sxs-lookup"><span data-stu-id="d8122-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="d8122-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d8122-110">Data Type</span></span>

<span data-ttu-id="d8122-111">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8122-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d8122-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8122-112">Remarks</span></span>

<span data-ttu-id="d8122-113">Das bevorzugte Attribut zum Angeben eines Genres ist [**WM/Genre**](wm-genre.md).</span><span class="sxs-lookup"><span data-stu-id="d8122-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="d8122-114">Verwenden Sie diese Einstellung für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="d8122-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="d8122-115">Wenn Sie in einer MP3-Datei entweder **WM/Genre** oder **WM/GenreID** ändern, wird das andere Attribut entsprechend geändert.</span><span class="sxs-lookup"><span data-stu-id="d8122-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="d8122-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d8122-116">Example</span></span>



| <span data-ttu-id="d8122-117">Dateityp</span><span class="sxs-lookup"><span data-stu-id="d8122-117">File type</span></span> | <span data-ttu-id="d8122-118">Beispielwert</span><span class="sxs-lookup"><span data-stu-id="d8122-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="d8122-119">Audio</span><span class="sxs-lookup"><span data-stu-id="d8122-119">Audio</span></span>     | <span data-ttu-id="d8122-120">"(4) Euro Disco"</span><span class="sxs-lookup"><span data-stu-id="d8122-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d8122-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8122-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8122-122">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="d8122-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




