---
title: Speichern eines 64-Bit-Werts
description: Verwenden Sie zum Speichern eines 64-Bit-Zeiger Werts ULONG \_ ptr. Ein ULONG- \_ ptr-Wert ist 32 Bits, wenn er mit einem 32-Bit-Compiler und 64 Bits kompiliert wird, wenn er mit einem 64-Bit-Compiler kompiliert wird.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- Speichern von 64-Bit-Werten für die Windows-Programmierung mit 64 Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310056"
---
# <a name="storing-a-64-bit-value"></a><span data-ttu-id="ef994-105">Speichern eines 64-Bit-Werts</span><span class="sxs-lookup"><span data-stu-id="ef994-105">Storing a 64-bit Value</span></span>

<span data-ttu-id="ef994-106">Verwenden Sie zum Speichern eines 64-Bit-Zeiger Werts **ulong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="ef994-106">To store a 64-bit pointer value, use **ULONG\_PTR**.</span></span> <span data-ttu-id="ef994-107">Ein **ulong- \_ ptr** -Wert ist 32 Bits, wenn er mit einem 32-Bit-Compiler und 64 Bits kompiliert wird, wenn er mit einem 64-Bit-Compiler kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="ef994-107">A **ULONG\_PTR** value is 32 bits when compiled with a 32-bit compiler and 64 bits when compiled with a 64-bit compiler.</span></span>

<span data-ttu-id="ef994-108">In den folgenden Beispielen wird realer Code verwendet, der in 64-Bit-Windows portiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ef994-108">The following examples use real-world code that has been ported to 64-bit Windows.</span></span> <span data-ttu-id="ef994-109">Kommentare zu den Schritten, mit denen der Code 64-Bit-kompatibel gemacht werden kann, sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef994-109">Commentary on the steps to make the code 64-bit compatible is included.</span></span>

## <a name="example-1-getting-an-address"></a><span data-ttu-id="ef994-110">Beispiel 1: erhalten einer Adresse</span><span class="sxs-lookup"><span data-stu-id="ef994-110">Example 1: Getting an Address</span></span>

<span data-ttu-id="ef994-111">Der folgende Code veranschaulicht eine Portier bare Methode, um eine Adresse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef994-111">The following code illustrates a portable way to get an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef994-112">Verwenden von ULONG (eine 32-Bit-Methode)</span><span class="sxs-lookup"><span data-stu-id="ef994-112">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef994-113">Verwenden von ULONG_PTR (die Portable-Methode)</span><span class="sxs-lookup"><span data-stu-id="ef994-113">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a><span data-ttu-id="ef994-114">Beispiel 2: Berechnen einer Adresse</span><span class="sxs-lookup"><span data-stu-id="ef994-114">Example 2: Calculating an Address</span></span>

<span data-ttu-id="ef994-115">Der folgende Code veranschaulicht eine portablen Methode zum Berechnen einer Adresse.</span><span class="sxs-lookup"><span data-stu-id="ef994-115">The following code illustrates a portable way to calculate an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef994-116">Verwenden von ULONG (eine 32-Bit-Methode)</span><span class="sxs-lookup"><span data-stu-id="ef994-116">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef994-117">Verwenden von ULONG_PTR (die Portable-Methode)</span><span class="sxs-lookup"><span data-stu-id="ef994-117">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




