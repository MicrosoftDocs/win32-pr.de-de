---
description: Die Header Datei "winternl. h" stellt Prototypen interner Windows-APIs zur Verfügung. Es gibt keine zugeordnete Import Bibliothek, sodass Entwickler Lauf Zeit dynamische Verknüpfungen verwenden müssen, um die in dieser Header Datei beschriebenen Funktionen aufzurufen.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Aufrufen interner APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958330"
---
# <a name="calling-internal-apis"></a><span data-ttu-id="107ce-104">Aufrufen interner APIs</span><span class="sxs-lookup"><span data-stu-id="107ce-104">Calling Internal APIs</span></span>

<span data-ttu-id="107ce-105">Die Header Datei "winternl. h" stellt Prototypen interner Windows-APIs zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="107ce-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="107ce-106">Es gibt keine zugeordnete Import Bibliothek, sodass Entwickler Lauf Zeit dynamische Verknüpfungen verwenden müssen, um die in dieser Header Datei beschriebenen Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="107ce-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="107ce-107">Die Funktionen und Strukturen in "winternl. h" sind für das Betriebssystem intern und können von einer Version von Windows zum nächsten und möglicherweise sogar zwischen Service Packs für die einzelnen Releases geändert werden.</span><span class="sxs-lookup"><span data-stu-id="107ce-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="107ce-108">Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, sollten Sie stattdessen die entsprechenden öffentlichen Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="107ce-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="107ce-109">Weitere Informationen finden Sie in der Header Datei, winternl. h, und in der Dokumentation zu den einzelnen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="107ce-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="107ce-110">Wenn Sie diese Funktionen verwenden, können Sie über die dynamische Lauf Zeit Verknüpfung mithilfe von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="107ce-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="107ce-111">Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="107ce-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="107ce-112">Signatur Änderungen sind jedoch möglicherweise nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="107ce-112">Signature changes, however, may not be detectable.</span></span>

 

 
