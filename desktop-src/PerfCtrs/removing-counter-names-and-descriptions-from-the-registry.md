---
description: Das unlodctr-Tool entfernt die von lodctr erstellten Registrierungseinträge.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Entfernen von Counter-Namen und Beschreibungen aus der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363469"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="966df-103">Entfernen von Counter-Namen und Beschreibungen aus der Registrierung</span><span class="sxs-lookup"><span data-stu-id="966df-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="966df-104">Das **unlodctr** -Tool entfernt die von **Lodctr** erstellten Registrierungseinträge.</span><span class="sxs-lookup"><span data-stu-id="966df-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="966df-105">Der Name der Anwendung, die Sie an **unlodctr** übergeben, muss mit dem [Namen des Anwendungs Schlüssels](creating-the-applications-performance-key.md) , den Sie unter dem **Dienst** Schlüssel erstellt haben, identisch sein.</span><span class="sxs-lookup"><span data-stu-id="966df-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="966df-106">Ausführliche Informationen zum Ausführen von **unlodctr** finden Sie unter Hilfe und Support Center.</span><span class="sxs-lookup"><span data-stu-id="966df-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="966df-107">Verwenden von unlodctr</span><span class="sxs-lookup"><span data-stu-id="966df-107">Using unlodctr</span></span>

<span data-ttu-id="966df-108">Das **unlodctr** -Tool sucht den ersten und den letzten Indikator und unterstützt die Indexwerte mithilfe der benannten Registrierungs Werte unter dem **Leistungs** Schlüssel Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="966df-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="966df-109">Das **unlodctr** **-Tool** verwendet den Bereich der Indexwerte, um den Text aus den Indikatoren und den **Hilfe** Werten für die einzelnen Sprachen Bezeichner zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="966df-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="966df-110">Durch die Verwendung der Indexwerte nimmt **unlodctr** die folgenden Änderungen an der Registrierung vor.</span><span class="sxs-lookup"><span data-stu-id="966df-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

<span data-ttu-id="966df-111">Das **unlodctr** -Tool entfernt auch die Werte für " **Counter**", " **Last Counter**", " **First Help**", " **Last Help**" und " **Object List** " aus dem **Leistungs** Schlüssel der Anwendung unter **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **Performance**.</span><span class="sxs-lookup"><span data-stu-id="966df-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="966df-112">Die Entlade Funktion von **unlodctr**, [**unloadperfcountertextstrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), wird in "LoadPerf. h" deklariert und aus Loadperf.dll exportiert.</span><span class="sxs-lookup"><span data-stu-id="966df-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="966df-113">Dies ermöglicht es Ihnen, diese Funktion direkt über das Deinstallationsprogramm aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="966df-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



