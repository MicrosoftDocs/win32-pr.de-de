---
description: Monitore können mithilfe der Netzwerkmonitor-Benutzeroberfläche konfiguriert werden. Endbenutzer können Konfigurations Kriterien an den Monitor übergeben, indem Sie ein HTML-Formular verwenden, das als htm-Datei im folgenden Unterordner des installierten Netzwerkmonitor SDK gespeichert ist.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Monitor Konfiguration (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89125450fc71bba21250a66f5c5458317138899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959017"
---
# <a name="monitor-configuration-network-monitor"></a><span data-ttu-id="3c099-104">Monitor Konfiguration (Netzwerkmonitor)</span><span class="sxs-lookup"><span data-stu-id="3c099-104">Monitor Configuration (Network Monitor)</span></span>

<span data-ttu-id="3c099-105">Monitore können mithilfe der Netzwerkmonitor-Benutzeroberfläche konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3c099-105">Monitors can be configured using the Network Monitor UI.</span></span> <span data-ttu-id="3c099-106">Endbenutzer können Konfigurations Kriterien an den Monitor übergeben, indem Sie ein HTML-Formular verwenden, das als htm-Datei im folgenden Unterordner des installierten Netzwerkmonitor SDK gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3c099-106">End-users can pass configuration criteria to your monitor using an HTML form stored as an HTM file in the following sub folder of your installed Network Monitor SDK.</span></span>

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

<span data-ttu-id="3c099-107">Wenn ein Endbenutzer die Schaltfläche **Monitor Konfiguration festlegen** auswählt, generiert der Browser eine HTML- **Post** -Nachricht, die die Namen und Werte für alle HTML-Formularelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="3c099-107">When an end user selects the **Set Monitor Configuration** button, the browser generates an HTML **POST** message, which includes the names and values for all the HTML form elements.</span></span>

<span data-ttu-id="3c099-108">Wenn die mcsvc die [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode aufruft, verweist der *pconfiguration* -Parameter auf die Daten aus der Post-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3c099-108">When the MCSVC calls the [IMonitor::DoConfigure](imonitor-doconfigure.md) method, the *pConfiguration* parameter points to the data from the POST message.</span></span> <span data-ttu-id="3c099-109">Der folgende Beispielcode stellt ein Beispiel für Nachrichten Nachrichten bereit:</span><span class="sxs-lookup"><span data-stu-id="3c099-109">The following example code provides an example of POST message data:</span></span>

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Diese Daten werden als lange ASCII-Zeichenfolge weitergegeben. Die Zeichenfolge ist für Ihre Länge und Darstellung von Abschnitten wie% 3a% 5C und% 0D% 0A von besonderer Art. Diese Besonderheit wird durch HTML verursacht, das erfordert, dass eine Methode alle möglichen ANSI-, DBCS-und Unicode-Zeichen folgen in ein ASCII-Format eingefügt. Beispielsweise fügt die **doconfigure** -Methode bestimmte Zeichen (z. b. das kaufmännische und-Zeichen (&) vor den einzelnen Variablennamen ein, um Sie als Variablennamen zu identifizieren. % 3a% 5C ist eine codierte Form des Doppelpunkt Zeichens, und% 0D% 0A gibt ein Wagen Rücklauf/Zeilenvorschub-Paar an. <span data-ttu-id="3c099-115">Der folgende Beispielcode stellt den resultierenden HTML-Code bereit, der vom Monitor interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="3c099-115">The following example code provides the resulting HTML code as interpreted by the monitor.</span></span>

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



