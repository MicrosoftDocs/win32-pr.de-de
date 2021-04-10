---
description: Anwendungen können Minidump-Dateien im Benutzermodus entwickeln, die eine nützliche Teilmenge der in einer Absturz Abbild Datei enthaltenen Informationen enthalten.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Minidumpdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126061"
---
# <a name="minidump-files"></a><span data-ttu-id="68404-103">Minidumpdateien</span><span class="sxs-lookup"><span data-stu-id="68404-103">Minidump Files</span></span>

<span data-ttu-id="68404-104">Anwendungen können Minidump-Dateien im Benutzermodus entwickeln, die eine nützliche Teilmenge der in einer Absturz Abbild Datei enthaltenen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="68404-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="68404-105">Anwendungen können minidumpdateien sehr schnell und effizient erstellen.</span><span class="sxs-lookup"><span data-stu-id="68404-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="68404-106">Da minidumpdateien klein sind, können Sie problemlos über das Internet an den technischen Support für die Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="68404-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="68404-107">Eine Minidumpdatei enthält nicht so viele Informationen wie eine vollständige Absturz Abbild Datei, Sie enthält jedoch genug Informationen, um grundlegende debuggingvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="68404-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="68404-108">Um eine Minidump-Datei zu lesen, müssen die Binärdateien und Symbol Dateien für den Debugger verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="68404-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="68404-109">Die aktuellen Versionen von Microsoft Office und Microsoft Windows erstellen minidumpdateien zum Zweck der Analyse von Fehlern auf den Computern der Kunden.</span><span class="sxs-lookup"><span data-stu-id="68404-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="68404-110">Die folgenden dbghelp-Funktionen werden mit Minidump-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="68404-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="68404-111">**Minidumpcallback**</span><span class="sxs-lookup"><span data-stu-id="68404-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="68404-112">**Minidumpreaddumpstream**</span><span class="sxs-lookup"><span data-stu-id="68404-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="68404-113">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="68404-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



