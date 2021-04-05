---
description: Der WDM-Anbieter (Windows-Treibermodell) gewährt den Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem WDM-Modell entsprechen.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: WDM-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753712"
---
# <a name="wdm-provider"></a>WDM-Anbieter

Der WDM-Anbieter (Windows-Treibermodell) gewährt den Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem WDM-Modell entsprechen. Die Klassen für Hardwaretreiber befinden sich im "root \\ WMI-Namespace".

WDM-Klassen werden primär in "WMI. mof" definiert.

WDM ist eine Betriebssystem Schnittstelle, über die Hardwarekomponenten Informationen und Ereignis Benachrichtigungen bereitstellen. Der WDM-Anbieter ist eine Klasse, eine Instanz, ein Ereignis und ein Methoden Anbieter, die Verwaltungs Anwendungen den Zugriff auf Daten und Ereignisse von WMI-for-WDM-fähigen Gerätetreibern ermöglicht. Die Klassen, die vom WDM-Anbieter zur Darstellung von Gerätetreiber Daten erstellt werden, befinden sich nur im \\ Namespace "root WMI". Dieser Namespace muss bereits vorhanden sein, bevor der WDM-Anbieter die installierten WDM-Treiber verarbeitet.

Der WDM-Anbieter zeichnet Informationen zu WDM-Vorgängen in der Datei wmiprov. log auf. Weitere Informationen finden Sie unter [WMI-Protokolldateien](/windows/desktop/WmiSdk/wmi-log-files).

Als Klasse, Instanz, Methode und Ereignis Anbieter implementiert der WDM-Anbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle sowie die folgenden [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Methoden:

-   [**"Kreateclassen"-Sequenz**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**"Kreateingestanceenumasync"**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Der WDM-Anbieter unterstützt das [**wmievent**](/windows/desktop/WmiCoreProv/wmievent) -System externe-Ereignis, das WMI über Ereignisse von WDM-basierten Treibern benachrichtigt. Sie können Ihre Ereignisconsumer für **wmievent** -Ereignisse wie jedes andere Ereignis registrieren. Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](/windows/desktop/WmiSdk/receiving-a-wmi-event). Beim Starten eines Treibers werden keine Klassen Erstellungs Ereignisse ausgelöst.

Der WDM-Anbieter unterstützt die folgende Klasse:

-   [**Wmibinarymufresource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Zugreifen auf Daten von Gerätetreibern](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
