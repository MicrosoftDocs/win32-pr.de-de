---
description: Die openperformancedata-Funktion der Leistungs-DLLs nimmt ein Zeichen folgen Argument als Eingabe an.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Erstellen anderer Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959767"
---
# <a name="creating-other-registry-entries"></a><span data-ttu-id="08b06-103">Erstellen anderer Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="08b06-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="08b06-104">Die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion der Leistungs-DLL nimmt als Eingabe ein Zeichen folgen Argument an.</span><span class="sxs-lookup"><span data-stu-id="08b06-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="08b06-105">Um eine Eingabe Zeichenfolge für die Open-Funktion bereitzustellen, fügen Sie einen **Verknüpfungs** Schlüssel unter Ihrem **Dienst** Schlüssel ein.</span><span class="sxs-lookup"><span data-stu-id="08b06-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="08b06-106">Der **Verknüpfungs** Schlüssel enthält einen **Export** Wert.</span><span class="sxs-lookup"><span data-stu-id="08b06-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="08b06-107">Legen Sie die Wertdaten für **Export** in die Eingabe Zeichenfolge fest, die Sie an die Open-Funktion übergeben möchten.</span><span class="sxs-lookup"><span data-stu-id="08b06-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="08b06-108">Der Datentyp des **Exports** lautet **" \_ reg \_ MultiSZ**".</span><span class="sxs-lookup"><span data-stu-id="08b06-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="08b06-109">Wenn **Export** nicht definiert ist (der **Export** ist optional), übergibt das System **null** an die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="08b06-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="08b06-110">Wenn mehr als eine Anwendung dieselbe Leistungs-DLL gemeinsam nutzt, enthält jede Anwendung in der Regel einen **Verknüpfungs** Schlüssel und einen **Export** Wert, um Kontext anzugeben, welche Anwendung die DLL aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="08b06-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="08b06-111">Im folgenden werden die Registrierungseinträge angezeigt:</span><span class="sxs-lookup"><span data-stu-id="08b06-111">The following shows the registry entries:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

<span data-ttu-id="08b06-112">Standardmäßig müssen die [**openperformancedata**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) -und [**collectperformancedata**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) -Funktionen der Leistungs-DLL innerhalb von 10.000 Millisekunden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08b06-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="08b06-113">Wenn dies nicht der Wert ist, verwendet das System nicht die von der DLL zurückgegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="08b06-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="08b06-114">Die Anwendung kann den Timeout Wert erhöhen oder verringern, indem Sie unter Ihrem **Leistungs** Schlüssel einen Registrierungs Wert für das **Öffnen von Timeout** oder einen **Timeout** Wert für den Registrierungs Wert angibt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08b06-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

<span data-ttu-id="08b06-115">Zum Abrufen der Leistungsdaten für einige Anwendungen (solche, die Leistungsindikatoren mithilfe der [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion zurückgeben) ist es erforderlich [**, die Funktion "-Funktion"**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zu verwenden, um das Gerät zu öffnen, das der Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08b06-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="08b06-116">In diesem Fall muss der in " **kreatefile** " angegebene Name auch im Knoten "DOS-Geräte" der Registrierung installiert werden, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="08b06-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
