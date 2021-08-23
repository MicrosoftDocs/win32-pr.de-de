---
description: Der WDM-Anbieter (Windows Driver Model) gewährt Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardwaretreibern, die dem WDM-Modell entsprechen.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: WDM-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ba187680ec371f331aa6394c5a2408c23080259e6b275e74cee496dd5125cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794620"
---
# <a name="wdm-provider"></a>WDM-Anbieter

Der WDM-Anbieter (Windows Driver Model) gewährt Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardwaretreibern, die dem WDM-Modell entsprechen. Die Klassen für Hardwaretreiber befinden sich im \\ "wmi-Stammnamespace".

WDM-Klassen werden hauptsächlich in Wmi.mof definiert.

WDM ist eine Betriebssystemschnittstelle, über die Hardwarekomponenten Informationen und Ereignisbenachrichtigungen bereitstellen. Der WDM-Anbieter ist ein Klassen-, Instanz-, Ereignis- und Methodenanbieter, der Verwaltungsanwendungen den Zugriff auf Daten und Ereignisse von WMI-for-WDM-fähigen Gerätetreibern ermöglicht. Die vom WDM-Anbieter zur Darstellung von Gerätetreiberdaten erstellten Klassen befinden sich nur im \\ Namespace "Root WMI". Dieser Namespace muss bereits vorhanden sein, bevor der WDM-Anbieter die installierten WDM-Treiber verarbeitet.

Der WDM-Anbieter zeichnet Informationen zu WDM-Vorgängen in der Datei WmiProv.log auf. Weitere Informationen finden Sie unter [WMI-Protokolldateien.](/windows/desktop/WmiSdk/wmi-log-files)

Als Klassen-, Instanz-, Methoden- und Ereignisanbieter implementiert der WDM-Anbieter die [**IWbemProviderInit-Standardschnittstelle**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) sowie die folgenden [**IWbemServices-Methoden:**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Der WDM-Anbieter unterstützt das [**WMIEvent-Extrinsische**](/windows/desktop/WmiCoreProv/wmievent) Ereignis, das WMI über Ereignisse von WDM-basierten Treibern benachrichtigt. Sie können Ihre Ereignisverbraucher wie jedes andere Ereignis für **WMIEvent-Ereignisse** registrieren. Weitere Informationen finden Sie unter [Empfangen eines WMI-Ereignisses.](/windows/desktop/WmiSdk/receiving-a-wmi-event) Beim Starten eines Treibers werden keine Ereignisse zur Klassenerstellung ausgelöst.

Der WDM-Anbieter unterstützt die folgende Klasse:

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Zugreifen auf Daten über Gerätetreiber](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
