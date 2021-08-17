---
description: Monitore können mithilfe der Netzwerkmonitor konfiguriert werden. Endbenutzer können Konfigurationskriterien an Ihren Monitor übergeben, indem sie ein HTML-Formular verwenden, das als HTM-Datei im folgenden Unterordner des installierten Netzwerkmonitor SDK gespeichert ist.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Überwachen der Konfiguration (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b55765774df3be2722c448a1af264162bcd9cdc51ac958cc555bf820d646b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364698"
---
# <a name="monitor-configuration-network-monitor"></a>Überwachen der Konfiguration (Netzwerkmonitor)

Monitore können mithilfe der Netzwerkmonitor konfiguriert werden. Endbenutzer können Konfigurationskriterien an Ihren Monitor übergeben, indem sie ein HTML-Formular verwenden, das als HTM-Datei im folgenden Unterordner des installierten Netzwerkmonitor SDK gespeichert ist.

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

Wenn ein Endbenutzer die  Schaltfläche Monitorkonfiguration festlegen auswählt, generiert der Browser eine HTML **POST-Nachricht,** die die Namen und Werte für alle HTML-Formularelemente enthält.

Wenn MCSVC die [IMonitor::D oConfigure-Methode](imonitor-doconfigure.md) aufruft, zeigt der *pConfiguration-Parameter* auf die Daten aus der POST-Nachricht. Der folgende Beispielcode enthält ein Beispiel für POST-Nachrichtendaten:

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Diese Daten werden als lange ASCII-Zeichenfolge übergeben. Die Zeichenfolge sieht sowohl in Ihrer Länge als auch in der Darstellung von Abschnitten wie %3A%5C und %0D%0A nicht sonderlich aus. Diese Elastizität wird durch HTML verursacht, was erfordert, dass eine Methode alle möglichen ANSI-, DBCS- und Unicode-Zeichenfolgen in ein ASCII-Format einstellt. Beispielsweise fügt die **DoConfigure-Methode** bestimmte Zeichen wie das ampersand (&) vor jedem Variablennamen ein, um ihn als Variablennamen zu identifizieren. %3A%5C ist eine codierte Form des Doppelpunktzeichens, und %0D%0A gibt ein Wagenrücklauf-/Zeilenfeedpaar an. Der folgende Beispielcode stellt den resultierenden HTML-Code wie vom Monitor interpretiert zur Verfügung.

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



