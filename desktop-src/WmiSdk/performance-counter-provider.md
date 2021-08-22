---
description: Der Leistungsindikatoranbieter ist ein Hochleistungsanbieter, der unformatte Leistungsindikatordaten für die von Win32 PerfRawData abgeleiteten WMI-Leistungsindikatorklassen \_ bietet. Der \_ \_ Win32Provider-Instanzname ist &\# 0034; NT5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Leistungsindikator-Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c846d66cd183e866623004cacfbcb630ac68480fab8dd58eca2b5a4dc6d2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050528"
---
# <a name="performance-counter-provider"></a>Leistungsindikator-Provider

\[Der Leistungsindikatoranbieter kann nicht mehr verwendet werden. Verwenden Sie stattdessen den [WMIPerfInst-Anbieter.](wmiperfinst-provider.md)\]

Der Leistungsindikatoranbieter ist ein Hochleistungsanbieter, der rohe Leistungsindikatordaten für die WMI-Leistungsindikatorklassen bietet, die von [**Win32 \_ PerfRawData abgeleitet werden.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) [](/windows/desktop/CIMWin32Prov/performance-counter-classes) Der [**\_ \_ Win32Provider-Instanzname**](--win32provider.md) ist "NT5 \_ GenericPerfProvider \_ V1".

Die [**Win32 \_ PerfRawData-Klassen**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) befinden sich im WMI-Namespace "Root \\ CIMv2". Jede WMI-Leistungsklasse entspricht einem Leistungsobjekt in einer Leistungsbibliothek. Die Eigenschaften dieser Klassen stellen die Leistungsindikatoren für das -Objekt dar. Der WMI-Klassenname für ein Unformat-Indikatorobjekt hat die Form **Win32 \_ \_ \_ PerfRawData-Dienstname* \_ *\_* \_ Objektname**. Der WMI-Klassenname, der die logischen Datenträgerzähler enthält, ist beispielsweise [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk.**](./retrieving-raw-and-formatted-performance-data.md)

Sie können die entsprechende [**Win32 \_ PerfFormattedData-Klasse**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) verwenden, um die vorab berechneten Leistungsdaten zu erhalten, die im [*Systemmonitor angezeigt werden.*](gloss-s.md) Verwenden Sie beispielsweise die [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk-Klasse,**](./retrieving-raw-and-formatted-performance-data.md) um vorab berechnete Datenträgerdaten zu erhalten.

Weitere Informationen zum Schreiben eines Clients, der auf Unformatierungsleistungsdaten zugreifen kann, finden Sie unter [Zugreifen auf Leistungsdaten in C++.](accessing-performance-data-in-c--.md)

Als Hochleistungsanbieter implementiert der Leistungsindikatoranbieter die [**IWbemProviderInit-Standardschnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) sowie die [**IWbemRefresher::Refresh-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) und die folgenden [**IWbemHiPerfProvider-Methoden:**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)

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

 

 
