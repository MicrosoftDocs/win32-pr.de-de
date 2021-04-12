---
title: Erstellen von Hardware Ereignis Abonnements
description: Auf Computern, auf denen ein Baseboard-Verwaltungs Controller (BMC) installiert ist, werden Hardware Ereignisse ausgelöst und im System Ereignisprotokoll (SEL) protokolliert, bei dem es sich um den BMC-Ereignisspeicher handelt, der in nichtflüchtigem Speicher gespeichert ist.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315915"
---
# <a name="creating-hardware-event-subscriptions"></a>Erstellen von Hardware Ereignis Abonnements

Auf Computern, auf denen ein Baseboard-Verwaltungs Controller (BMC) installiert ist, werden Hardware Ereignisse ausgelöst und im System Ereignisprotokoll (SEL) protokolliert, bei dem es sich um den BMC-Ereignisspeicher handelt, der in nichtflüchtigem Speicher gespeichert ist. Um diese Hardware Ereignisse unter Windows Server 2008 mithilfe des Ereignisanzeige zu lesen, müssen Sie ein Abonnement für die Ereignisse erstellen. Die Hardware Ereignis Abonnements funktionieren nur auf Windows Server 2008.

Das folgende Verfahren definiert, wie das SEL-Ereignis Abonnement zum Abrufen der Hardware Ereignisse erstellt wird:

1.  Speichern Sie den folgenden XML-Code in einer XML-Datei (in diesem Beispiel heißt die Datei Wsmanselrg.xml). Dieser XML-Code definiert das Abonnement.

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

    

2.  Erstellen Sie ein Ereignis Abonnement, indem Sie den folgenden Befehl in einem Eingabe Aufforderungs Fenster ausführen (das Wecutil.exe Programm befindet sich im Verzeichnis% systemroot% \\ system32.):

    **Wecutil** - *<path> \\wsmanselrg.xml*

3.  Stellen Sie sicher, dass das Abonnement aktiv ist, indem Sie den folgenden Befehl in einem Eingabe Aufforderungs Fenster ausführen:

    **Wecutil GR** *wsmanselrg*

Der BMC ist ein lokal an einen Server angefügter Mikrocontroller. BMCs verfügen über Sensoren, die den physischen Zustand des Servers und eine separate Netzwerkverbindung überwachen, die über das Netzwerk kommunizieren kann, auch wenn der Server offline ist. Sie haben Zugriff auf BMC-Daten über den WMI-Anbieter (Intelligent Platform Management Interface). Weitere Informationen zum IPMI-Anbieter finden Sie unter [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

Auf dem Computer muss der BMC und der IPMI-Anbieter installiert sein, damit das Ereignis Abonnement funktioniert. Für Computer, die unter Windows Server 2008 ausgeführt werden, wird der IPMI-Anbieter standardmäßig installiert. Wenn der BMC nicht verfügbar ist, kann der IPMI-Treiber nicht installiert werden, und der Abonnement Lauf Zeit Status zeigt immer einen Fehler an (0x8004001-WMI Generic Failure).

 

 