---
description: Der Leistungsindikatorenanbieter ist ein Hochleistungs Anbieter, der Rohdaten des Leistungs Zählers für die von Win32 perfrawdata abgeleiteten Klassen von WMI-Leistungs Zählern bereitstellt \_ . Der \_ \_ Win32Provider-Instanzname ist &\# 0034; NT5 \_ genericperfprovider \_ v1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Leistungsindikator-Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050469"
---
# <a name="performance-counter-provider"></a>Leistungsindikator-Provider

\[Der Leistungsindikatorenanbieter ist nicht mehr zur Verwendung verfügbar. Verwenden Sie stattdessen den [wmiperfinst](wmiperfinst-provider.md) -Anbieter.\]

Der Leistungsindikatorenanbieter ist ein Hochleistungs Anbieter, der Rohdaten des Leistungs Zählers für die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)abgeleiteten Klassen von WMI- [Leistungs Zählern](/windows/desktop/CIMWin32Prov/performance-counter-classes) bereitstellt. Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname lautet "NT5 \_ genericperfprovider \_ v1".

Die [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen befinden sich im WMI- \\ Namespace "root CIMv2". Jede WMI-Leistungsklasse entspricht einem Leistungs Objekt in einer Leistungs Bibliothek. Die Eigenschaften dieser Klassen stellen die Leistungsindikatoren für das-Objekt dar. Der WMI-Klassenname für ein unformatierte Counter-Objekt hat das Format **Win32 \_ \_ \_ perfrawdata* Service \_ Name *\_* Object \_ Name * * *. Der WMI-Klassenname, der die Leistungsindikatoren für logische Datenträger enthält, lautet beispielsweise [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

Sie können die entsprechende [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klasse verwenden, um die im [*System Monitor*](gloss-s.md)angezeigten vorab berechneten Leistungsdaten zu erhalten. Verwenden Sie z. b. die [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse, um vorab berechnete Datenträger Daten zu erhalten.

Weitere Informationen zum Schreiben eines Clients, der auf rohleistungs Daten zugreifen kann, finden Sie unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md).

Als Hochleistungs Anbieter implementiert der Leistungsindikatorenanbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode und die folgenden [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) -Methoden:

-   [**"Kreaterefreshableaufzählung"**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**"Kreaterefreshableobject"**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**Anmelde Fresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**Queryinstance**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**Stopp Aktualisierung**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 
