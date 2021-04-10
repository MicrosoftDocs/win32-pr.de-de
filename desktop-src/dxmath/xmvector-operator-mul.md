---
description: Multiplikations Operatoren
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: Operator *-Operatoren
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130581"
---
# <a name="operator--operators"></a><span data-ttu-id="e1cd1-103">Operator \* Operatoren</span><span class="sxs-lookup"><span data-stu-id="e1cd1-103">operator \* operators</span></span>

<span data-ttu-id="e1cd1-104">Multiplikations Operator</span><span class="sxs-lookup"><span data-stu-id="e1cd1-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="e1cd1-105">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="e1cd1-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e1cd1-106">Operator</span><span class="sxs-lookup"><span data-stu-id="e1cd1-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e1cd1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1cd1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e1cd1-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>Xmvector:: Operator \* (float, xmvector)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1cd1-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e1cd1-109">Multiplizieren eines Gleit Komma Werts durch eine Instanz von <code>XMVECTOR</code> , wobei das Ergebnis einer neuen Instanz von zurückgegeben wird <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="e1cd1-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="e1cd1-110"><code>operator \*</code>Multipliziert einen Gleit Komma Wert für jede Komponente einer Instanz des <a href="xmvector-data-type.md"><strong>xmvector-Datentyps</strong></a>und gibt eine neue-Instanz zurück, <code>XMVECTOR</code> deren Komponenten das Ergebnis enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cd1-111">Dieser Operator ist nur unter C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e1cd1-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>Xmvector:: Operator \* (xmvector, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1cd1-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e1cd1-113">Multiplizieren Sie eine Instanz von <code>XMVECTOR</code> mit einem Gleit Komma Wert, und geben Sie das Ergebnis einer neuen Instanz von zurück <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="e1cd1-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="e1cd1-114"><code>operator \*</code>Multipliziert jede Komponente einer Instanz des <a href="xmvector-data-type.md"><strong>xmvector-Datentyps</strong></a> mit einem Gleit Komma Wert und gibt eine neue-Instanz zurück, <code>XMVECTOR</code> deren Komponenten das Ergebnis enthalten.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cd1-115">Dieser Operator ist nur unter C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e1cd1-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>Xmvector:: Operator \* (xmvector, xmvector)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e1cd1-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e1cd1-117">Multipliziert eine Instanz von <code>XMVECTOR</code> mit einer zweiten-Instanz und gibt das Ergebnis in einer dritten-Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="e1cd1-118"><code>operator \*</code>Multipliziert jede Komponente einer Instanz des <a href="xmvector-data-type.md"><strong>xmvector-Datentyps</strong></a> mit der entsprechenden Komponente in einer zweiten Instanz von <code>XMVECTOR</code> und gibt eine neue-Instanz zurück, <code>XMVECTOR</code> die das Ergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e1cd1-119">Dieser Operator ist nur unter C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1cd1-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="e1cd1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1cd1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cd1-121">Xmvector-Operatoren</span><span class="sxs-lookup"><span data-stu-id="e1cd1-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="e1cd1-122">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e1cd1-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1cd1-123">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e1cd1-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
