---
description: Thread Umgebungs Block (debugnotizen)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Thread Umgebungs Block (debugnotizen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861143"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="e40c0-103">Thread Umgebungs Block (debugnotizen)</span><span class="sxs-lookup"><span data-stu-id="e40c0-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="e40c0-104">Der Thread Umgebungs Block ([**TEB-Struktur**](/windows/win32/api/winternl/ns-winternl-teb)) enthält Kontextinformationen für einen Thread.</span><span class="sxs-lookup"><span data-stu-id="e40c0-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="e40c0-105">In den folgenden Versionen von Windows beträgt der Offset der 32-Bit-TEB-Adresse innerhalb des 64-Bit-TEB 0.</span><span class="sxs-lookup"><span data-stu-id="e40c0-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="e40c0-106">Dies kann für den direkten Zugriff auf das 32-Bit-TEB eines WOW64-Threads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e40c0-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="e40c0-107">Dies ändert sich möglicherweise in späteren Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="e40c0-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="e40c0-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e40c0-108">Windows Vista</span></span> | <span data-ttu-id="e40c0-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e40c0-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="e40c0-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e40c0-110">Windows 7</span></span>     | <span data-ttu-id="e40c0-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e40c0-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="e40c0-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e40c0-112">Windows 8</span></span>     | <span data-ttu-id="e40c0-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e40c0-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="e40c0-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e40c0-114">Windows 8.1</span></span>   | <span data-ttu-id="e40c0-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e40c0-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e40c0-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e40c0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e40c0-117">Debuggen von Strukturen</span><span class="sxs-lookup"><span data-stu-id="e40c0-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="e40c0-118">**WOW64- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="e40c0-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
