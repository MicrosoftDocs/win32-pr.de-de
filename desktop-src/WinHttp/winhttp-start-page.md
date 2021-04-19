---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) stellen Entwicklern eine HTTP-Client-API (Application Programming Interface) zum Senden von Anforderungen über das HTTP-Protokoll an andere HTTP-Server zur Verfügung.
ms.assetid: 354ab65d-5e46-451d-b36b-2f8166a1a048
title: Windows HTTP-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f03a3204257410e4db0182724ab63743116f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350440"
---
# <a name="windows-http-services"></a><span data-ttu-id="3cb5f-103">Windows HTTP-Dienste</span><span class="sxs-lookup"><span data-stu-id="3cb5f-103">Windows HTTP Services</span></span>

## <a name="purpose"></a><span data-ttu-id="3cb5f-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="3cb5f-104">Purpose</span></span>

<span data-ttu-id="3cb5f-105">Die Microsoft Windows HTTP-Dienste (WinHTTP) stellen Entwicklern eine HTTP-Client-API (Application Programming Interface) zum Senden von Anforderungen über das HTTP-Protokoll an andere HTTP-Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-105">Microsoft Windows HTTP Services (WinHTTP) provides developers with an HTTP client application programming interface (API) to send requests through the HTTP protocol to other HTTP servers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3cb5f-106">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="3cb5f-106">Where applicable</span></span>

<span data-ttu-id="3cb5f-107">WinHTTP unterstützt Desktop Client Anwendungen, Windows-Dienste und Windows Server-basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-107">WinHTTP supports desktop client applications, Windows services, and Windows server-based applications.</span></span>

<span data-ttu-id="3cb5f-108">Weitere Informationen zur Verwendung von WinHTTP für Anwendungen, die auf Microsoft .NET Framework basieren, finden Sie in der [winhttphandler-API](/dotnet/api/system.net.http?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="3cb5f-108">For more information on how to use WinHTTP for applications built on the Microsoft .NET Framework, see the [WinHttpHandler API](/dotnet/api/system.net.http?view=netframework-4.8)</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3cb5f-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="3cb5f-109">Developer audience</span></span>

<span data-ttu-id="3cb5f-110">WinHTTP bietet sowohl eine C/C++-API (Application Programming Interface) als auch eine Component Object Model (com)-Automatisierungskomponente, die für die Verwendung in ASP-basierten Anwendungen (Active Server Pages) geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-110">WinHTTP offers both a C/C++ application programming interface (API) and a Component Object Model (COM) automation component suitable for use in Active Server Pages (ASP) based applications.</span></span>

<span data-ttu-id="3cb5f-111">Ein grundlegendes Verständnis des HTTP-Protokolls ist wichtig, um beide Schnittstellen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-111">A basic understanding of the HTTP protocol is important to use either interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3cb5f-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="3cb5f-112">Run-time requirements</span></span>

<span data-ttu-id="3cb5f-113">WinHTTP 5,1 bietet Verbesserungen gegenüber Version 5,0.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-113">WinHTTP 5.1 offers improvements over version 5.0.</span></span> <span data-ttu-id="3cb5f-114">Sie ist im Betriebssystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-114">It is included in the operating system.</span></span> <span data-ttu-id="3cb5f-115">Weitere Informationen zu neuen Features finden Sie unter neues [in WinHTTP 5,1](what-s-new-in-winhttp-5-1.md) und Neuerungen [in Windows Server 2008 und Windows Vista](what-s-new-in-windows-longhorn.md).</span><span class="sxs-lookup"><span data-stu-id="3cb5f-115">For more information about new features, see [What's New in WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) and [What's New in Windows Server 2008 and Windows Vista](what-s-new-in-windows-longhorn.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cb5f-116">Der WinHTTP 5,0-Download ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-116">The WinHTTP 5.0 download is no longer available.</span></span> <span data-ttu-id="3cb5f-117">Seit dem 1. Oktober 2004 hat Microsoft das WinHTTP 5,0 SDK-Download von MSDN entfernt und den Produktsupport für Version 5,0 beendet.</span><span class="sxs-lookup"><span data-stu-id="3cb5f-117">As of October 1, 2004, Microsoft removed the WinHTTP 5.0 SDK download from MSDN and terminated product support for version 5.0.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="3cb5f-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3cb5f-118">In this section</span></span>

-   [<span data-ttu-id="3cb5f-119">Informationen zu WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cb5f-119">About WinHTTP</span></span>](about-winhttp.md)
-   [<span data-ttu-id="3cb5f-120">Verwenden von WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3cb5f-120">Using WinHTTP</span></span>](using-winhttp.md)
-   [<span data-ttu-id="3cb5f-121">WinHTTP-Referenz</span><span class="sxs-lookup"><span data-stu-id="3cb5f-121">WinHTTP Reference</span></span>](winhttp-reference.md)

 

 
