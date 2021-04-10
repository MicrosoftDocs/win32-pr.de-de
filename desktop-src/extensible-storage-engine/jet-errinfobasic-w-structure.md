---
description: 'Weitere Informationen finden Sie hier: JET_ERRINFOBASIC_W Struktur'
title: JET_ERRINFOBASIC_W Struktur
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961782"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="77630-103">JET_ERRINFOBASIC_W Struktur</span><span class="sxs-lookup"><span data-stu-id="77630-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="77630-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77630-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="77630-105">JET_ERRINFOBASIC_W Struktur</span><span class="sxs-lookup"><span data-stu-id="77630-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="77630-106">Die **JET_ERRINFOBASIC_W** -Struktur definiert die Daten, die von der [jetgeterrorinfo ()](./jetgeterrorinfow-function.md) -Methode zurückgegeben werden, wenn die JET_ErrorInfoSpecificErr infolevel-Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="77630-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="77630-107">Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage-Engine.</span><span class="sxs-lookup"><span data-stu-id="77630-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="77630-108">Diese Informationen können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="77630-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="77630-109">Member</span><span class="sxs-lookup"><span data-stu-id="77630-109">Members</span></span>

<span data-ttu-id="77630-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="77630-110">**cbStruct**</span></span>

<span data-ttu-id="77630-111">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="77630-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="77630-112">Er muss auf sizeof (JET_ERRINFOBASIC) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77630-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="77630-113">**errvalue**</span><span class="sxs-lookup"><span data-stu-id="77630-113">**errValue**</span></span>

<span data-ttu-id="77630-114">Der auszuwertende Fehlerwert, wie für das *pvresult* -Argument an [jetgeterrorinfo ()](./jetgeterrorinfow-function.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="77630-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="77630-115">**Err| mustspecific**</span><span class="sxs-lookup"><span data-stu-id="77630-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="77630-116">Die [JET_ERRCAT](./jet-errcat.md) Konstante der untersten Ebene, die dem Fehler zugeordnet ist. Das heißt, die Kategorie auf Blatt Ebene in der Kategoriehierarchie, die in [JET_ERRCAT](./jet-errcat.md)dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="77630-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="77630-117">**rgkategoricalhierarchy \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="77630-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="77630-118">Die Hierarchie von Fehlerkategorien, die dem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="77630-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="77630-119">Position 0 ist die höchste Ebene in der Hierarchie von [JET_ERRCAT](./jet-errcat.md), und der Rest sind Unterkategorien, bis die spezifischere Kategorie festgelegt ist, nach der alle Kategorien JET_errcatUnknown werden.</span><span class="sxs-lookup"><span data-stu-id="77630-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="77630-120">**lsourceline**</span><span class="sxs-lookup"><span data-stu-id="77630-120">**lSourceLine**</span></span>

<span data-ttu-id="77630-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="77630-121">Reserved.</span></span>

<span data-ttu-id="77630-122">**rgszsourcefile \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="77630-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="77630-123">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="77630-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="77630-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77630-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77630-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="77630-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77630-126">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77630-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77630-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="77630-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77630-128">Erfordert Windows 8-Server.</span><span class="sxs-lookup"><span data-stu-id="77630-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77630-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="77630-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77630-130">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="77630-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
