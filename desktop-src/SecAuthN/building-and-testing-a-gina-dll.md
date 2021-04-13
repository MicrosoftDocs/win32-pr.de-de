---
description: Alle Funktionen, Prototypen, Strukturen und Konstanten werden in der Header Datei winwlx. h definiert.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Entwickeln und Testen einer Gina-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352048"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="16e53-103">Entwickeln und Testen einer Gina-dll</span><span class="sxs-lookup"><span data-stu-id="16e53-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="16e53-104">Alle Funktionen, Prototypen, Strukturen und Konstanten werden in der Header Datei winwlx. h definiert.</span><span class="sxs-lookup"><span data-stu-id="16e53-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="16e53-105">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="16e53-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="16e53-106">Verwenden Sie zum Testen einer [*Gina*](/windows/desktop/SecGloss/g-gly) -dll den Winlogon.exe aus einer überprüften Version des Betriebssystems, die mit dem Microsoft Windows Driver Development Kit (DDK) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="16e53-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="16e53-107">Die aktivierte Version von [*Winlogon*](/windows/desktop/SecGloss/w-gly) unterstützt das Debuggen von Ginas wie folgt:</span><span class="sxs-lookup"><span data-stu-id="16e53-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="16e53-108">Sie können die folgende Syntax verwenden, um einen Abschnitt in Win.ini zu erstellen, um Winlogon-Debugoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="16e53-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="16e53-109">Wenn angegeben, sollte **logfile** den voll qualifizierten Namen der Datei enthalten, die zum Protokollieren von Debuginformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16e53-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="16e53-110">Wenn die Datei nicht vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="16e53-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="16e53-111">Die **DebugFlags** -Optionen geben an, welche Arten von Debuginformationen in die Protokolldatei oder den Debugger geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="16e53-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="16e53-112">Debug- **Flags** können eines oder mehrere der folgenden Flags enthalten.</span><span class="sxs-lookup"><span data-stu-id="16e53-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="16e53-113">Debugflag</span><span class="sxs-lookup"><span data-stu-id="16e53-113">Debugging flag</span></span> | <span data-ttu-id="16e53-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16e53-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="16e53-115">Coolswitch</span><span class="sxs-lookup"><span data-stu-id="16e53-115">CoolSwitch</span></span>     | <span data-ttu-id="16e53-116">Die Tastenkombination STRG + ALT + UMSCHALT + TAB bewirkt eine debugpause in Winlogon.</span><span class="sxs-lookup"><span data-stu-id="16e53-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="16e53-117">Fehler</span><span class="sxs-lookup"><span data-stu-id="16e53-117">Error</span></span>          | <span data-ttu-id="16e53-118">Fehler drucken.</span><span class="sxs-lookup"><span data-stu-id="16e53-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="16e53-119">Init</span><span class="sxs-lookup"><span data-stu-id="16e53-119">Init</span></span>           | <span data-ttu-id="16e53-120">Druck Initialisierungs-und Fortschrittsmeldungen.</span><span class="sxs-lookup"><span data-stu-id="16e53-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="16e53-121">Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="16e53-121">Notify</span></span>         | <span data-ttu-id="16e53-122">Meldungen zum Druck Benachrichtigungs Paket.</span><span class="sxs-lookup"><span data-stu-id="16e53-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="16e53-123">SAS</span><span class="sxs-lookup"><span data-stu-id="16e53-123">SAS</span></span>            | <span data-ttu-id="16e53-124">Druckt Informationen über SAS-Benachrichtigungen ( [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="16e53-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="16e53-125">State</span><span class="sxs-lookup"><span data-stu-id="16e53-125">State</span></span>          | <span data-ttu-id="16e53-126">Meldungen drucken, wenn sich der Zustand von Winlogon ändert.</span><span class="sxs-lookup"><span data-stu-id="16e53-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="16e53-127">Timeout</span><span class="sxs-lookup"><span data-stu-id="16e53-127">Timeout</span></span>        | <span data-ttu-id="16e53-128">Drucken von Nachrichten, wenn ein Zeitlimit festgelegt ist oder ein Zeitlimit erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="16e53-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="16e53-129">Trace</span><span class="sxs-lookup"><span data-stu-id="16e53-129">Trace</span></span>          | <span data-ttu-id="16e53-130">Ausführliche Ablauf Verfolgungs Informationen drucken.</span><span class="sxs-lookup"><span data-stu-id="16e53-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="16e53-131">Warnung</span><span class="sxs-lookup"><span data-stu-id="16e53-131">Warn</span></span>           | <span data-ttu-id="16e53-132">Druck Warnungen.</span><span class="sxs-lookup"><span data-stu-id="16e53-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="16e53-133">Fügen Sie den folgenden Eintrag in die Registrierung ein, um die überprüfte Version von Winlogon in einem Debugger zu starten:</span><span class="sxs-lookup"><span data-stu-id="16e53-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> <span data-ttu-id="16e53-134">Zum Debuggen von Winlogon müssen Sie den symbolischen Debugger (NNS) von Windows verwenden.</span><span class="sxs-lookup"><span data-stu-id="16e53-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16e53-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16e53-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e53-136">Laden und Ausführen einer Gina-dll</span><span class="sxs-lookup"><span data-stu-id="16e53-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="16e53-137">Gina-Export Funktionen</span><span class="sxs-lookup"><span data-stu-id="16e53-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="16e53-138">Gina-Strukturen</span><span class="sxs-lookup"><span data-stu-id="16e53-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="16e53-139">Terminal Dienste-Gina-Funktionen</span><span class="sxs-lookup"><span data-stu-id="16e53-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
