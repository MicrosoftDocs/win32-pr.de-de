---
description: Stellt Informationen zu einer Quell Code Datei dar.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Sourcefileingefo-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481990"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="019d3-103"><span id="vspixengine.sourcefileinfo"></span>Sourcefileingefo-Struktur</span><span class="sxs-lookup"><span data-stu-id="019d3-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="019d3-104">Stellt Informationen zu einer Quell Code Datei dar.</span><span class="sxs-lookup"><span data-stu-id="019d3-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="019d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="019d3-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="019d3-106">Member</span><span class="sxs-lookup"><span data-stu-id="019d3-106">Members</span></span>

<span data-ttu-id="019d3-107">**fileName**</span><span class="sxs-lookup"><span data-stu-id="019d3-107">**fileName**</span></span>  
<span data-ttu-id="019d3-108">Eine com-Zeichenfolge, die den filePath der zugeordneten Quelldatei komprimiert.</span><span class="sxs-lookup"><span data-stu-id="019d3-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="019d3-109">**checksumb-tecount**</span><span class="sxs-lookup"><span data-stu-id="019d3-109">**checksumByteCount**</span></span>  
<span data-ttu-id="019d3-110">Die Anzahl der Bytes in der Prüfsumme.</span><span class="sxs-lookup"><span data-stu-id="019d3-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="019d3-111">Wenn checksumalgorithm gleich checksumalgorithm:: MD5 ist, lautet checksumb-Zähler 16.</span><span class="sxs-lookup"><span data-stu-id="019d3-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="019d3-112">Wenn checksumalgorithm gleich checksumalgorithm:: SHA1 ist, lautet checksumb-Zähler 20.</span><span class="sxs-lookup"><span data-stu-id="019d3-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="019d3-113">**checksumalgorithm**</span><span class="sxs-lookup"><span data-stu-id="019d3-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="019d3-114">Gibt den Algorithmus an, der zum Generieren der Prüfsumme der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="019d3-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="019d3-115">Unterstützte Algorithmen sind MD5 und SHA1.</span><span class="sxs-lookup"><span data-stu-id="019d3-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="019d3-116">Weitere Informationen finden Sie unter checksumalgorithm-Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="019d3-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="019d3-117">**checksumfirstpart**</span><span class="sxs-lookup"><span data-stu-id="019d3-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="019d3-118">Der erste 8-Byte-Teil der Prüfsumme.</span><span class="sxs-lookup"><span data-stu-id="019d3-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="019d3-119">**checksumsecondpart**</span><span class="sxs-lookup"><span data-stu-id="019d3-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="019d3-120">Der zweite 8-Byte-Teil der Prüfsumme.</span><span class="sxs-lookup"><span data-stu-id="019d3-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="019d3-121">**checksumthirdpart**</span><span class="sxs-lookup"><span data-stu-id="019d3-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="019d3-122">Der dritte 8-Byte-Teil der Prüfsumme.</span><span class="sxs-lookup"><span data-stu-id="019d3-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="019d3-123">**checksumfourthpart**</span><span class="sxs-lookup"><span data-stu-id="019d3-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="019d3-124">Der vierte 8-Byte-Teil der Prüfsumme.</span><span class="sxs-lookup"><span data-stu-id="019d3-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="019d3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="019d3-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="019d3-126">Header</span><span class="sxs-lookup"><span data-stu-id="019d3-126">Header</span></span></p></td><td><span data-ttu-id="019d3-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="019d3-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



