---
description: Verwenden Sie die folgenden Funktionen, um Leistungsdaten zu nutzen und bereitzustellen.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Funktionen der Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349859"
---
# <a name="performance-counters-functions"></a>Funktionen der Leistungsindikatoren

Verwenden Sie die folgenden Funktionen, um Leistungsdaten zu nutzen und bereitzustellen.

## <a name="consumer-functions"></a>Consumer-Funktionen

### <a name="performance-data-helper-pdh-functions"></a>PDH-Funktionen (Performance Data Helper)

Verwenden Sie die Leistungsdaten Hilfsfunktionen (PDH), um Leistungsdaten von v1-und v2-Leistungsdaten Anbietern zu nutzen.

> [!Note]
> Windows onecore-Apps können die PDH-Funktionen nicht verwenden. Verwenden Sie beim Schreiben von Windows onecore-apps [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).

- [*Counterpathcallback*](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [**Pdhaddcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [**Pdhaddenglishcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [**Pdhbindinputdatasource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [**Pdhbrowpcounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [**Pdhbrowpcountersh**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [**Pdhcalculatecounterfromrawvalue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [**Pdhcloselog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [**Pdhclosequery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**Pdhcollectquerydata**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**Pdhcollectquerydataex**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [**Pdhcollectquerydatawithtime**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [**Pdhcomputecounterstatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [**Pdhconnectmachine**](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [**Pdhenumschlag logsetnames**](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [**Pdhenumschlag Machines**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [**Pdhenumschlag machinesh**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [**Pdhenumubjectitems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [**Pdhenumubjectitemsh**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [**Pdhenumubjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [**Pdhenumubjectsh**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [**Pdhexpandcounterpath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [**Pdhexpandwildcardpathh**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [**Pdhformatfromrawvalue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [**Pdhgetcounterinfo**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [**Pdhgetcountertimebase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [**Pdhgetdatasourcetimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [**PdhGetDataSourceTimeRangeH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [**Pdhgetdefaultperfcounter**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [**Pdhgetdefaultperfcounterh**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [**Pdhgetdefaultperfobject**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [**Pdhgetdefaultperfobjecth**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [**Pdhgetdllversion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [**Pdhgetformattedcounterarray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [**Pdhgetformattedcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [**Pdhgetlogfilesize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [**Pdhgetrawcounterarray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [**Pdhgetrawcountervalue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [**Pdhisrealtimequery**](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [**Pdhlookupperfindexbyname**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [**Pdhlookupperfnamebyindex**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [**Pdhmakecounterpath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [**Pdhoptolog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [**Pdhopumquery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [**Pdhopenqueryh**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [**Pdhparser-counterpath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [**Pdhparameseinstancename**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [**Pdhleserrawlogrecord**](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**Pdhselectdatasource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [**Pdhsetcounterscalefactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [**Pdhsetdefaultrealtimedatasource**](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [**Pdhsetquerytimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [**Pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [**Pdhupdatelogfilecatalog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [**Pdhvalidatepath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [**Pdhvalidatepathex**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a>Perflib v2-consumerfunktionen

Verwenden Sie die Perflib v2-consumerfunktionen, um Leistungsdaten von V2-Leistungsdaten Anbietern zu nutzen, wenn Sie die PDH-Funktionen (Performance Data Helper) nicht verwenden können. Diese Funktionen können verwendet werden, wenn Sie onecore-Anwendungen schreiben, um v2-Gegensätze zu erfassen, oder wenn Sie bestimmte v2-Gegensätze mit minimalen Abhängigkeiten und mehr Aufwand erfassen müssen.

> [!TIP]
> Die Perflib v2-consumerfunktionen sind schwieriger zu verwenden als die PDH-Funktionen (Performance Data Helper) und unterstützen nur das Sammeln von Daten von V2-Anbietern. Die PDH-Funktionen sollten für die meisten Anwendungen bevorzugt werden.

- [**Perfaddcounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [**Perfclosequeryhandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [**Perfdeletecounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [**Perfenumeratecounterset**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [**Perfenumeratecounterset-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [**Perfopenqueryhandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [**Perfquerycounterdata**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [**Perfquerycounterinfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [**Perfquerycounterset tregistrationinfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a>Anbieter Funktionen

### <a name="perflib-v2-provider-functions"></a>Perflib v2-Anbieter Funktionen

[V2-Leistungsdaten Anbieter](providing-counter-data-using-version-2-0.md) verwenden die folgenden Funktionen:

- [*"Belegcatememory"*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [*Controlcallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [**Gegen Cleanup**](countercleanup.md)
- [**Gegen initialisieren**](counterinitialize.md)
- [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [**Perfkreateingestance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [**Perfdecrementulongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [**Perfdecrementulonglongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [**Perfdelta eteinstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [**Perfinkrementulongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [**Perfinkrementulonglongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [**Perfqueryinstance**](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [**Perfsetcountersetinfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [**Perfsetulongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [**Perfsetulonglongcountervalue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [**Perfsetcounterref-Wert**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [**Perfstartprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [**Perfstartproviderex**](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [**Perfstopprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> Verwenden Sie zum Installieren und Deinstallieren von V2-Anbietern die Tools **Lodctr** und **unlodctr** . Die Funktionen **LoadPerfCounterTextStrings** und **unloadperfcountertextstrings** können nicht zum Installieren und Deinstallieren von V2-Anbietern verwendet werden.

### <a name="performance-dll-functions"></a>Leistungs-DLL-Funktionen

[V1-Leistungsdaten Anbieter](providing-counter-data-using-a-performance-dll.md) implementieren eine DLL, die die folgenden Funktionen bereitstellt:

- [*ClosePerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [*CollectPerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- [*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

> [!Note]
> Aufgrund erheblicher Leistungs-und Zuverlässigkeitsprobleme sind v1-Leistungsdaten Anbieter veraltet. Obwohl Sie weiterhin eine Leistungs Erweiterungs-DLL zum Bereitstellen von Leistungsdaten verwenden können, wird empfohlen, stattdessen [einen v2-Anbieter zu erstellen](providing-counter-data-using-version-2-0.md) . Außerdem wird empfohlen, vorhandene v1-Anbieter durch v2-Anbieter zu ersetzen.

V1-Anbieter können mithilfe der Tools **Lodctr** und **unlodctr** oder durch Aufrufen der folgenden Funktionen installiert und deinstalliert werden:

- [**LoadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [**Unloadperfcountertextstrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
