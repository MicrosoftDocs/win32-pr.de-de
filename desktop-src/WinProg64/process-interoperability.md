---
title: Prozess Interoperabilität
description: Sie können Win32-basierte Anwendungen auf 64-Bit-Windows mithilfe einer Emulations Schicht ausführen. Windows 10 auf ARM umfasst eine x86-on-ARM64-Emulations Schicht. Weitere Informationen finden Sie unter Ausführen von 32-Bit-Anwendungen.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- Prozess Interoperabilität 64-Bit-Windows-Programmierung
- Interoperabilität 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338391"
---
# <a name="process-interoperability"></a><span data-ttu-id="daf09-107">Prozess Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="daf09-107">Process Interoperability</span></span>

<span data-ttu-id="daf09-108">Sie können Win32-basierte Anwendungen auf 64-Bit-Windows mithilfe einer Emulations Schicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="daf09-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="daf09-109">Windows 10 auf ARM umfasst eine x86-on-ARM64-Emulations Schicht.</span><span class="sxs-lookup"><span data-stu-id="daf09-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="daf09-110">Weitere Informationen finden Sie unter [Ausführen von 32-Bit-Anwendungen](running-32-bit-applications.md).</span><span class="sxs-lookup"><span data-stu-id="daf09-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="daf09-111">Bei 64-Bit-Fenstern kann ein 64-Bit-Prozess keine 32-Bit-DLL (Dynamic-Link Library) laden.</span><span class="sxs-lookup"><span data-stu-id="daf09-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="daf09-112">Außerdem kann ein 32-Bit-Prozess keine 64-Bit-DLL laden.</span><span class="sxs-lookup"><span data-stu-id="daf09-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="daf09-113">64-Bit-Windows unterstützt jedoch remote Prozedur Aufrufe (Remote Procedure Calls, RPC) zwischen 64-Bit-und 32-Bit-Prozessen (auf demselben Computer und Computer übergreifend).</span><span class="sxs-lookup"><span data-stu-id="daf09-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="daf09-114">Auf 64-Bit-Fenstern kann ein Prozess interner 32-Bit-COM-Server mit einem 64-Bit-Client kommunizieren, und ein Prozess interner 64-Bit-COM-Server kann mit einem 32-Bit-Client kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="daf09-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="daf09-115">Wenn Sie also über eine 32-Bit-DLL verfügen, die nicht com-fähig ist, können Sie Sie in einem Prozess externen COM-Server einschließen und com verwenden, um Aufrufe von und von einem 64-Bit-Prozess zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="daf09-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="daf09-116">Prozess interne Server werden zurzeit mit dem Registrierungs Eintrag **InprocServer** registriert.</span><span class="sxs-lookup"><span data-stu-id="daf09-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="daf09-117">Auf 64-Bit-Windows-Servern sollten 64-und 32-Bit-Prozess interne Server den Eintrag **InProcServer32** verwenden.</span><span class="sxs-lookup"><span data-stu-id="daf09-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="daf09-118">Verwenden Sie zum Portieren von Handles, die in ihrer Art lokal auf dem Computer sind und nie über die 32-Bit-zu-64-Bit-Grenze verwendet werden, den **handle- \_ ptr** -Typ anstelle des **int- \_ ptr** -oder **DWORD- \_ ptr** -Typs.</span><span class="sxs-lookup"><span data-stu-id="daf09-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="daf09-119">Dies umfasst das Portieren von RPC-Schnittstellen, die solche Handles als **DWORD** -Werte übergeben</span><span class="sxs-lookup"><span data-stu-id="daf09-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="daf09-120">Das 64-Bit- **handle " \_ ptr** " ist im Netzwerk 64 Bits (nicht abgeschnitten) und benötigt daher keine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="daf09-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="daf09-121">(Das 32-Bit- **handle \_ ptr** ist 32 Bits.)</span><span class="sxs-lookup"><span data-stu-id="daf09-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="daf09-122">Weitere Informationen finden Sie unter [Entwerfen von 64-Bit-kompatiblen Schnittstellen](designing-64-bit-compatible-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="daf09-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




