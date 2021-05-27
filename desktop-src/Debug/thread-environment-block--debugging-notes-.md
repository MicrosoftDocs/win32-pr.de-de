---
description: Threadumgebungsblock (Debughinweise)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Threadumgebungsblock (Debughinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550585"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="72ed8-103">Threadumgebungsblock (Debughinweise)</span><span class="sxs-lookup"><span data-stu-id="72ed8-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="72ed8-104">Der Threadumgebungsblock [**(TEB-Struktur)**](/windows/win32/api/winternl/ns-winternl-teb)enthält Kontextinformationen für einen Thread.</span><span class="sxs-lookup"><span data-stu-id="72ed8-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="72ed8-105">In den folgenden Versionen von Windows ist der Offset der 32-Bit-TEB-Adresse innerhalb des 64-Bit-TEB 0.</span><span class="sxs-lookup"><span data-stu-id="72ed8-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="72ed8-106">Dies kann verwendet werden, um direkt auf den 32-Bit-TEB eines WOW64-Threads zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="72ed8-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="72ed8-107">Dies kann sich in späteren Versionen von Windows ändern.</span><span class="sxs-lookup"><span data-stu-id="72ed8-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="72ed8-108">Plattform</span><span class="sxs-lookup"><span data-stu-id="72ed8-108">Platform</span></span>     | <span data-ttu-id="72ed8-109">Version</span><span class="sxs-lookup"><span data-stu-id="72ed8-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="72ed8-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72ed8-110">Windows Vista</span></span> | <span data-ttu-id="72ed8-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72ed8-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="72ed8-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="72ed8-112">Windows 7</span></span>     | <span data-ttu-id="72ed8-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72ed8-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="72ed8-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="72ed8-114">Windows 8</span></span>     | <span data-ttu-id="72ed8-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72ed8-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="72ed8-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72ed8-116">Windows 8.1</span></span>   | <span data-ttu-id="72ed8-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="72ed8-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="72ed8-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72ed8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72ed8-119">Debuggen von Strukturen</span><span class="sxs-lookup"><span data-stu-id="72ed8-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="72ed8-120">**\_WOW64-KONTEXT**</span><span class="sxs-lookup"><span data-stu-id="72ed8-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
