---
title: Treiber (Programmier Handbuch für 64-Bit-Windows)
description: Die 64-Bit-Version von Windows ist darauf ausgelegt, Entwicklern die Verwendung einer einzelnen Quell Code Basis für Ihre 32-Bit-und 64-Bit-Anwendungen zu ermöglichen. In großem Umfang gilt dies auch für 32-Bit-und 64-Bit-Windows-Treiber.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- Treiber 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340208"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="5f32a-105">Treiber (Programmier Handbuch für 64-Bit-Windows)</span><span class="sxs-lookup"><span data-stu-id="5f32a-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="5f32a-106">Die 64-Bit-Version von Windows ist darauf ausgelegt, Entwicklern die Verwendung einer einzelnen Quell Code Basis für Ihre 32-Bit-und 64-Bit-Anwendungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5f32a-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="5f32a-107">In großem Umfang gilt dies auch für 32-Bit-und 64-Bit-Windows-Treiber.</span><span class="sxs-lookup"><span data-stu-id="5f32a-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="5f32a-108">32-Bit-Treiber können jedoch nicht auf 64-Bit-Fenstern ausgeführt werden und müssen portiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f32a-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="5f32a-109">Für Benutzermodusanwendungen enthält 64-Bit-Windows WOW64, das die Ausführung von 32-Bit-Windows-Anwendungen ermöglicht (mit einem gewissen Leistungsverlust) auf Systemen, auf denen 64-Bit-Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f32a-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="5f32a-110">Für Treiber ist keine äquivalente übersetzungsebene vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5f32a-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="5f32a-111">Informationen zum Portieren von Treibern in 64-Bit-Windows finden Sie unter [64-Bit-Probleme](https://msdn.microsoft.com/library/aa489627.aspx) im Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="5f32a-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




