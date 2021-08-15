---
title: Erstellen von Hardwareereignisabonnements
description: Auf Computern, auf denen ein Baseboard Management Controller (BMC) installiert ist, werden Hardwareereignisse ausgelöst und im Systemereignisprotokoll (System Event Log, SEL) protokolliert. Dabei handelt es sich um den BMC-Ereignisspeicher, der im nicht unwillingsfreien Speicher gespeichert ist.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ee32d590143ed8a1ffacec6f59ad3b3094c2d2a22d0df66b0cb0d3521f83e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751112"
---
# <a name="creating-hardware-event-subscriptions"></a>Erstellen von Hardwareereignisabonnements

Auf Computern, auf denen ein Baseboard Management Controller (BMC) installiert ist, werden Hardwareereignisse ausgelöst und im Systemereignisprotokoll (System Event Log, SEL) protokolliert. Dabei handelt es sich um den BMC-Ereignisspeicher, der im nicht unwillingsfreien Speicher gespeichert ist. Um diese Hardwareereignisse auf Windows Server 2008 mithilfe des Ereignisanzeige zu lesen, müssen Sie ein Abonnement für die Ereignisse erstellen. Die Hardwareereignisabonnements funktionieren nur auf Windows Server 2008.

Das folgende Verfahren definiert, wie das SEL-Ereignisabonnement zum Abrufen der Hardwareereignisse erstellt wird:

1.  Speichern Sie den folgenden XML-Code in .xml Datei (in diesem Beispiel heißt die Datei Wsmanselrg.xml). Dieser XML-Code definiert das Abonnement.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  Erstellen Sie ein Ereignisabonnement, indem Sie den folgenden Befehl in einem Eingabeaufforderungsfenster ausführen (das Wecutil.exe-Programm befindet sich im Verzeichnis %SYSTEMROOT% \\ System32):

    **Wecutil cs** *<path> \\wsmanselrg.xml*

3.  Stellen Sie sicher, dass das Abonnement aktiv ist, indem Sie den folgenden Befehl in einem Eingabeaufforderungsfenster ausführen:

    **Wecutil gr** *wsmanselrg*

Der BMC ist ein Mikrocontroller, der lokal an einen Server angefügt ist. BMCs verfügen über Sensoren, die den physischen Zustand des Servers überwachen, und eine separate Netzwerkverbindung, die über das Netzwerk kommunizieren kann, auch wenn der Server offline ist. Sie haben Zugriff auf BMC-Daten über den WMI-Anbieter (Intelligent Platform Management Interface, IPMI). Weitere Informationen zum IPMI-Anbieter finden Sie unter [IPMI-Anbieter.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

Auf dem Computer müssen der BMC und der IPMI-Anbieter installiert sein, damit das Ereignisabonnement funktioniert. Für Computer, die auf Windows Server 2008 ausgeführt werden, wird der IPMI-Anbieter standardmäßig installiert. Wenn der BMC nicht verfügbar ist, kann der IPMI-Treiber nicht installiert werden, und der Laufzeitstatus des Abonnements zeigt immer einen Fehler an (0x8004001 – Generischer WMI-Fehler).

 

 