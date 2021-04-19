---
description: Die folgenden Operatoren werden von der xmvector-Struktur verfügbar gemacht.
ms.assetid: 16fc1276-7bed-4e6f-8af5-d871afa73b68
title: Xmvector-Operatoren
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0611be5e9737e2829bc06f9a3fade10db233cbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372934"
---
# <a name="xmvector-operators"></a><span data-ttu-id="a29f9-103">Xmvector-Operatoren</span><span class="sxs-lookup"><span data-stu-id="a29f9-103">XMVECTOR Operators</span></span>

<span data-ttu-id="a29f9-104">Die folgenden Operatoren werden von der [**xmvector**](xmvector-data-type.md) -Struktur verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a29f9-104">The following operators are exposed by the [**XMVECTOR**](xmvector-data-type.md) structure.</span></span>

> [!Note]  
> <span data-ttu-id="a29f9-105">Die hier aufgeführten Operatoren sind nur unter C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a29f9-105">The operators listed here are only available under C++.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="a29f9-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a29f9-106">In this section</span></span>



| <span data-ttu-id="a29f9-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="a29f9-107">Methods</span></span>                                                    | <span data-ttu-id="a29f9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a29f9-108">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a29f9-109">[**Operator + =**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a29f9-109">[**operator +=**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span></span><br/>  | <span data-ttu-id="a29f9-110">Fügt einer Instanz einen Gleit Komma Wert hinzu `XMVECTOR` und gibt einen Verweis auf die aktualisierte-Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="a29f9-110">Adds a floating point value to an `XMVECTOR` instance, and returns a reference to the updated instance.</span></span> <br/>                         |
| <span data-ttu-id="a29f9-111">[**Operator-=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a29f9-111">[**operator -=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span></span><br/>    | <span data-ttu-id="a29f9-112">Subtrahiert einen Gleit Komma Wert von der aktuellen Instanz von `XMVECTOR` und gibt das Ergebnis in der aktualisierten aktuellen Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="a29f9-112">Subtracts a floating point value from the current instance of `XMVECTOR`, returning the result in the updated current instance.</span></span> <br/> |
| [<span data-ttu-id="a29f9-113">\**Operator \** _</span><span class="sxs-lookup"><span data-stu-id="a29f9-113">\**operator \** _</span></span>](xmvector-operator-mul.md)<br/>    | <span data-ttu-id="a29f9-114">Multiplikations Operator</span><span class="sxs-lookup"><span data-stu-id="a29f9-114">Multiplication operators</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a29f9-115">*Operator \* =* _\*</span><span class="sxs-lookup"><span data-stu-id="a29f9-115">_ *operator \*=*\*</span></span>](xmvector-operator-muleq.md)<br/> | <span data-ttu-id="a29f9-116">Multiplikations Zuweisung</span><span class="sxs-lookup"><span data-stu-id="a29f9-116">Multiplication assignment operators</span></span><br/>                                                                                              |
| [<span data-ttu-id="a29f9-117">**KOM**</span><span class="sxs-lookup"><span data-stu-id="a29f9-117">**operator /**</span></span>](xmvector-operator-div.md)<br/>     | <span data-ttu-id="a29f9-118">Divisionsoperator</span><span class="sxs-lookup"><span data-stu-id="a29f9-118">Division operator.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="a29f9-119">**Operator/=**</span><span class="sxs-lookup"><span data-stu-id="a29f9-119">**operator /=**</span></span>](xmvector-operator-diveq.md)<br/>  | <span data-ttu-id="a29f9-120">Divisions Zuweisungs Operator.</span><span class="sxs-lookup"><span data-stu-id="a29f9-120">Division Assignment operator.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="a29f9-121">**KOM**</span><span class="sxs-lookup"><span data-stu-id="a29f9-121">**operator -**</span></span>](xmvector-operator--.md)<br/>       | <span data-ttu-id="a29f9-122">Subtraktions-und Negations Operatoren</span><span class="sxs-lookup"><span data-stu-id="a29f9-122">Subtraction and negation operators</span></span><br/>                                                                                               |
| [<span data-ttu-id="a29f9-123">**Operator +**</span><span class="sxs-lookup"><span data-stu-id="a29f9-123">**operator +**</span></span>](xmvector-operator-pls.md)<br/>     | <span data-ttu-id="a29f9-124">Addition-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="a29f9-124">Addition operators.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="a29f9-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a29f9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a29f9-126">Xmvector-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a29f9-126">XMVECTOR Extensions</span></span>](ovw-xmvector-extensions.md)
</dt> <dt>

<span data-ttu-id="a29f9-127">**Typen**</span><span class="sxs-lookup"><span data-stu-id="a29f9-127">**Types**</span></span>
</dt> <dt>

[<span data-ttu-id="a29f9-128">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a29f9-128">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
