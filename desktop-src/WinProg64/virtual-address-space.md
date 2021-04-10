---
title: Virtueller Adressraum (Programmier Handbuch für 64-Bit-Windows)
description: Standardmäßig haben 64-Bit-Microsoft Windows-basierte Anwendungen einen Adressraum im Benutzermodus von mehreren Terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, virtueller Adressraum
- virtueller Adressraum 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039910"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="74591-105">Virtueller Adressraum (Programmier Handbuch für 64-Bit-Windows)</span><span class="sxs-lookup"><span data-stu-id="74591-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="74591-106">Standardmäßig haben 64-Bit-Microsoft Windows-basierte Anwendungen einen Adressraum im Benutzermodus von mehreren Terabytes.</span><span class="sxs-lookup"><span data-stu-id="74591-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="74591-107">Genaue Werte finden Sie unter Arbeits [Speicher Grenzwerte für Windows-und Windows Server-Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span><span class="sxs-lookup"><span data-stu-id="74591-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="74591-108">Anwendungen können jedoch angeben, dass das System den gesamten Arbeitsspeicher für die Anwendung unterhalb von 2 Gigabyte zuordnen soll.</span><span class="sxs-lookup"><span data-stu-id="74591-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="74591-109">Diese Funktion ist für 64-Bit-Anwendungen vorteilhaft, wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="74591-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="74591-110">Ein 2-GB-Adressraum ist ausreichend.</span><span class="sxs-lookup"><span data-stu-id="74591-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="74591-111">Der Code weist viele Warnungen für das Abschneiden von Zeigern auf.</span><span class="sxs-lookup"><span data-stu-id="74591-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="74591-112">Zeiger und ganze Zahlen sind frei gemischt.</span><span class="sxs-lookup"><span data-stu-id="74591-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="74591-113">Der Code weist Polymorphie mithilfe von 32-Bit-Datentypen auf.</span><span class="sxs-lookup"><span data-stu-id="74591-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="74591-114">Alle Zeiger sind immer noch 64-Bit-Zeiger, aber das System stellt sicher, dass jede Speicher Belegung unter dem Grenzwert von 2 GB liegt, sodass, wenn die Anwendung einen Zeiger abschneidet, keine signifikanten Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="74591-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="74591-115">Zeiger können auf 32-Bit-Werte gekürzt und dann auf 64-Bit-Werte durch Vorzeichen Erweiterung oder NULL erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="74591-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="74591-116">Um diese Speicherbeschränkung anzugeben, verwenden Sie die Option **/LARGEADDRESSAWARE: No** Linker.</span><span class="sxs-lookup"><span data-stu-id="74591-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="74591-117">Beachten Sie, dass **/LARGEADDRESSAWARE: No** für eine ARM64-Binärdatei ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="74591-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="74591-118">Beachten Sie jedoch, dass Probleme auftreten können, wenn Sie diese Option verwenden.</span><span class="sxs-lookup"><span data-stu-id="74591-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="74591-119">Wenn Sie eine DLL erstellen, die diese Option verwendet, und die dll von einer Anwendung aufgerufen wird, die diese Option nicht verwendet, kann die dll einen 64-Bit-Zeiger abschneiden, dessen obere 32 Bits wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="74591-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="74591-120">Dies kann zu einem Anwendungsfehler führen, ohne dass eine Warnung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="74591-120">This can cause application failure without any warning.</span></span>

 

 
