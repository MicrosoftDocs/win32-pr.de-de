---
description: Berechnete Liefer (&\# 0034; gekocht&\# 0034;) Leistungsdaten des Leistungs Zählers. Stellt dynamische Daten für die WMI-Klassen bereit, die von Win32 \_ perfformatteddata abgeleitet werden. Wird auch als gekochte gegen Anbieter bezeichnet.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Formatierte Leistungs Datenanbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360190"
---
# <a name="formatted-performance-data-provider"></a>Formatierte Leistungs Datenanbieter

\[Die formatierte Leistungs Datenanbieter, auch bekannt als "gekochte Leistungs Anbieter", ist nicht mehr zur Verwendung verfügbar. Verwenden Sie stattdessen den [wmiperfinst](wmiperfinst-provider.md) -Anbieter.\]

Der leistungsfähige Hochleistungs Datenanbieter liefert berechnete ("gekochte") Leistungsdaten, z. b. den Prozentsatz der Zeit, die ein Datenträger für das Schreiben von Daten benötigt. Dieser Anbieter stellt dynamische Daten für die WMI-Klassen bereit, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet werden. Der Unterschied zwischen diesem Anbieter und dem [Leistungsindikatorenanbieter](performance-counter-provider.md) besteht darin, dass der Leistungsindikatorenanbieter Rohdaten bereitstellt und [](gloss-s.md)der gekochte Leistungsindikatoren Leistungsdaten liefert Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname ist "hiperfkocher \_ v1".

Der WMI-formatierte Klassenname für ein Counter-Objekt hat die Form "Win32 \_ perfformatteddata \_ *Service \_ Name* \_ *Object \_ Name*". Der WMI-Klassenname, der die Leistungsindikatoren für logische Datenträger enthält, lautet beispielsweise **Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**. Diese Klassen befinden sich im \\ Namespace "root CIMv2".

Da Leistungsdaten Klassen auf einem bestimmten System dynamisch hinzugefügt und geändert werden, ist es nicht möglich, die Eigenschaften aller bekannten Leistungs Objekte formal zu dokumentieren. Informationen dazu, welche Klassen für Sie verfügbar sind, und um zu ermitteln, welche Member diese Klassen haben, finden Sie unter [Abrufen der Dokumentation für Rohdaten und formatierte Leistungsdaten Objekte](retrieving-raw-and-formatted-performance-data.md).

Die [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen verwenden den **cookingtype** -Qualifizierer in [WMI-Leistungsdaten Typen](wmi-performance-counter-types.md) , um die Formel für die Berechnung der Leistungsdaten anzugeben. Dieser Qualifizierer ist mit dem **CounterType** -Qualifizierer in den [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen identisch.

Als Hochleistungs Anbieter implementiert der gekochte Leistungs Anbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die [**iwbemrefresh Sher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) -Methode und die folgenden [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) -Methoden:

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

 

 
