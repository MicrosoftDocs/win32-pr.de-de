---
description: Eine Anwendung, die Leistungsindikatoren unterstützt, muss unter dem Dienst Schlüssel über einen Leistungs Schlüssel verfügen. Das folgende Beispiel zeigt die Werte, die Sie für diesen Schlüssel einschließen müssen.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Erstellen des Anwendungs Leistungs Schlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348015"
---
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="d5722-104">Erstellen des Leistungs Schlüssels der Anwendung</span><span class="sxs-lookup"><span data-stu-id="d5722-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="d5722-105">Eine Anwendung, die Leistungsindikatoren unterstützt, muss unter dem **Dienst** Schlüssel über einen **Leistungs** Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="d5722-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="d5722-106">Das folgende Beispiel zeigt die Werte, die Sie für diesen Schlüssel einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="d5722-106">The following example shows the values that you must include for this key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

<span data-ttu-id="d5722-107">Der **Bibliotheks** Wert gibt den Namen der Leistungs-DLL an, und die Werte " **Open**", " **Collect**" und " **Close** " stellen die Namen der Funktionen bereit, die von der Leistungs-DLL exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="d5722-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="d5722-108">Der Datentyp dieser Werte ist **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="d5722-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="d5722-109">Wenn ein Consumer Leistungsdaten anfordert, verwendet das System diese Werte, um zu bestimmen, welche Leistungs-DLLs geladen und welche DLL-Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5722-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="d5722-110">Der **Bibliotheks** Wert kann den DLL-Namen oder einen vollständigen Pfad zur dll enthalten.</span><span class="sxs-lookup"><span data-stu-id="d5722-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="d5722-111">Wenn Sie den reg-Datentyp "reg" für die **Bibliothek** verwenden, können Sie Umgebungsvariablen in Ihrem Pfad angeben. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="d5722-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="d5722-112">Der Dienst Schlüssel der Anwendung muss vorhanden sein, bevor Sie **Lodctr** ausführen können, um ihre Namen und Hilfe Zeichenfolgen zu laden.</span><span class="sxs-lookup"><span data-stu-id="d5722-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="d5722-113">Weitere Registrierungs Werte, die Sie erstellen können, wie z. b. das Angeben von Timeout Werten für die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion und die [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktion, finden Sie unter [Erstellen anderer Registrierungseinträge](creating-other-registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="d5722-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
