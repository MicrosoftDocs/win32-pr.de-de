---
title: COM-Handler
description: Der Zweck von com-Handlern ist die Angabe von \ 0034; Intelligent \ 0034; Code im Client Adressraum, der Aufrufe zwischen einem Client und einem Server optimieren kann. Handler können einige Schnittstellen überschreiben und andere direkt an den Server delegieren (über den Proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341832"
---
# <a name="com-handlers"></a><span data-ttu-id="c4026-104">COM-Handler</span><span class="sxs-lookup"><span data-stu-id="c4026-104">COM Handlers</span></span>

<span data-ttu-id="c4026-105">Der Zweck von com-Handlern besteht darin, einen "intelligenten" Code im Client Adressraum bereitzustellen, der Aufrufe zwischen einem Client und einem Server optimieren kann.</span><span class="sxs-lookup"><span data-stu-id="c4026-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="c4026-106">Handler können einige Schnittstellen überschreiben und andere direkt an den Server delegieren (über den Proxy).</span><span class="sxs-lookup"><span data-stu-id="c4026-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="c4026-107">Es gibt zwei Arten von com-Handlern:</span><span class="sxs-lookup"><span data-stu-id="c4026-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="c4026-108">[Der OLE-Handler](the-ole-handler.md) ist eine umfangreich-dll, die wichtige Dienste zum Verknüpfen und Einbetten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c4026-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="c4026-109">Sie wird in der Regel vor dem Starten des Servers erstellt und initialisiert, sodass der Server aktiviert wird, wenn das eingebettete Objekt in den Zustand wird ausgeführt wechselt.</span><span class="sxs-lookup"><span data-stu-id="c4026-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="c4026-110">[Der Lightweight-Client seitige Handler](the-lightweight-client-side-handler.md) kann für beliebige Zwecke erstellt werden, kann sehr klein sein und kann nicht vor dem Server erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4026-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




