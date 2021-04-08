---
description: Das Microsoft&\# 160; Der Win32-Anbieter ruft für Windows-Systeme relevante Daten&\# 8212 ab und aktualisiert diese, z. b. die aktuellen Einstellungen der Umgebungsvariablen und die Attribute eines logischen Datenträgers.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Win32-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747904"
---
# <a name="win32-provider"></a>Win32-Anbieter

Der Microsoft Win32-Anbieter ruft für Windows-Systeme relevante Daten ab und aktualisiert Sie – Daten, wie z. b. die aktuellen Einstellungen von Umgebungsvariablen und die Attribute eines logischen Datenträgers. Mit dem Win32-Anbieter können Verwaltungs Anwendungen WMI für den einfachen Zugriff auf diese Daten verwenden. Der Win32-Anbieter ruft seine Informationen mithilfe von Windows-Funktionsaufrufen und Abfragen der Systemregistrierung ab.

Der Win32-Anbieter definiert die Klassen, die zum Beschreiben von Hardware oder Software auf Windows-Systemen und deren Beziehungen verwendet werden.

Als Instanz-und Methoden Anbieter implementiert der Win32-Anbieter die standardmäßige [**iwbemproviderinit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die folgenden [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) -Methoden:

-   [**"Kreateingestanceenumasync"**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**Delta einstanceasync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

In der folgenden Tabelle sind die Kategorien der Win32-Anbieter Klassen aufgeführt.



| Klassen                                                                             | BESCHREIBUNG                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Computer System-Hardware Klassen](computer-system-hardware-classes.md)<br/> | Hardware bezogene Objekte.<br/>                                      |
| [Betriebssystemklassen](operating-system-classes.md)<br/>                 | Mit dem Betriebssystem verbundene Objekte.<br/>                              |
| [Leistungs Leistungsdaten-Klassen](performance-counter-classes.md)<br/>           | Rohdaten und berechnete Leistungsdaten aus Leistungsindikatoren.<br/> |
| [WMI-Dienst Verwaltungs Klassen](wmi-service-management-classes.md)<br/>     | Verwaltung für WMI.<br/>                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Cimwin32-WMI-Anbieter](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
