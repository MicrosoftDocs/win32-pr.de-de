---
description: Berechnete Dienstleistungen (&\# 0034;&\# 0034;) Leistungsindikatordaten. Stellt dynamische Daten für die WMI-Klassen zur Anwendung, die von Win32 \_ PerfFormattedData abgeleitet wurden. Wird auch als Anbieter des Kontrahentenzählers bezeichnet.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Formatierte Leistungsindikatoren Datenanbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab8e931c3d03c619af5b1e37cadd8dacdccd21534513ed3a1aa1d7b9076acfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556613"
---
# <a name="formatted-performance-data-provider"></a>Formatierte Leistungsindikatoren Datenanbieter

\[Die formatierte Datenanbieter, auch bekannt als "Anbieter von Kontrahentenzählern", steht nicht mehr zur Verwendung zur Verfügung. Verwenden Sie stattdessen den [WMIPerfInst-Anbieter.](wmiperfinst-provider.md)\]

Der Hochleistungsanbieter für formatierte Leistungsdaten stellt berechnete Leistungsindikatordaten ("1000") zur Verfügung, z. B. den Prozentsatz der Zeit, die ein Datenträger zum Schreiben von Daten verbringt. Dieser Anbieter stellt dynamische Daten für die WMI-Klassen zur Anwendung, die von [**Win32 \_ PerfFormattedData abgeleitet wurden.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) Der Unterschied zwischen diesem [](performance-counter-provider.md) Anbieter und dem Leistungsindikatoranbieter besteht in dem, dass der Leistungsindikatoranbieter Rohdaten und der Anbieter des Zählerzählers Leistungsdaten liefert, die genau wie im [*Systemmonitor angezeigt werden.*](gloss-s.md) Der [**\_ \_ Win32Provider-Instanzname**](--win32provider.md) ist "HiPerfCooker \_ v1".

Der WMI-formatierte Klassenname für ein Indikatorobjekt hat das Format "Win32 \_ PerfFormattedData \_ *\_ Dienstname* \_ *\_ Objektname*". Der WMI-Klassenname, der die logischen Datenträgerindikatoren enthält, ist beispielsweise **Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk.** Diese Klassen befinden sich im Namespace "Root \\ CIMv2".

Da Leistungsdatenklassen auf einem bestimmten System dynamisch hinzugefügt und geändert werden, ist es nicht möglich, die Eigenschaften aller bekannten Leistungsobjekte formal zu dokumentieren. Informationen dazu, welche Klassen für Sie verfügbar sind und welche Member diese Klassen haben, finden Sie unter Abrufen der Dokumentation für Unformatierte und [formatierte Leistungsdatenobjekte.](retrieving-raw-and-formatted-performance-data.md)

Die [**Win32 \_ PerfFormattedData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) verwenden den Qualifizierer **"Ungstyp"** in WMI-Leistungsindikatortypen, um die Formel zum Berechnen von Leistungsdaten anzugeben. [](wmi-performance-counter-types.md) Dieser Qualifizierer ist  mit dem CounterType-Qualifizierer in den [**Win32 \_ PerfRawData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) identisch.

Als Leistungsstarker Anbieter implementiert der Anbieter des Zählers Für Kontrahenten die [**IWbemProviderInit-Standardschnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) sowie die [**IWbemRefresher::Refresh-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) und die folgenden [**IWbemHiPerfProvider-Methoden:**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**Getobjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 
