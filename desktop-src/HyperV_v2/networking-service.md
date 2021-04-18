---
description: Das Netzwerk Profil beschreibt die Objekte, die zum Konfigurieren des Systems verwendet werden, damit virtuelle Maschinen über das Netzwerk kommunizieren können.
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: Netzwerkdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc85b7a5121a3e7e42f333f829816184b57bd8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347746"
---
# <a name="networking-service"></a>Netzwerkdienst

Das Netzwerk Profil beschreibt die Objekte, die zum Konfigurieren des Systems verwendet werden, damit virtuelle Maschinen über das Netzwerk kommunizieren können. Die globalen Netzwerk Objekte, die verwendet werden, um den Netzwerk Switch im Verwaltungs Betriebssystem zu konfigurieren, umfassen die Klassen [**MSVM \_ virtualethernetungwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md), [**MSVM \_ virtualethernetnotwitch**](msvm-virtualethernetswitch.md)und [**MSVM \_ ethernetungwitchport**](msvm-ethernetswitchport.md) . Die Netzwerk Objekte der virtuellen Maschine, die zum Konfigurieren der Netzwerkschnittstellenkarte (NIC) auf dem virtuellen Computer verwendet werden, enthalten die [**MSVM- \_ emulatedethernetport**](msvm-emulatedethernetport.md)-, [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md)-und [**MSVM \_ lanendpoint**](msvm-lanendpoint.md) -Klassen.

Der Stamm des globalen Netzwerk Profils ist die Klasse " [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) ". Diese Klasse stellt ein virtuelles switchgerät im Verwaltungs Betriebssystem dar. **MSVM \_ Virtualethernetungwitch** ist Instanzen der [**MSVM \_ Switchport**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) -Klasse zugeordnet, die die Ports auf dem virtuellen Switch darstellt. Instanzen der Klassen " **MSVM \_ virtualethernwitch** " und " [**MSVM \_ ethernettwitchport**](msvm-ethernetswitchport.md) " werden über die Klasse " [**MSVM \_ virtualethernettwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md) " erstellt, gelöscht und verbunden (in der obigen Abbildung nicht dargestellt).

Der Verwaltungsdienst für virtuelle Switches (VSMs) repräsentiert den Netzwerkdienst, der auf einem einzelnen Hyper-V-Host vorhanden ist, und enthält Methoden für den [**MSVM \_ virtualethernetswitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md) , der zum Steuern der Definition, Änderung und Zerstörung globaler Netzwerkressourcen wie virtuellen Switches, Switchports und internen Ethernet-Ports verwendet wird.

Die Darstellung des Ethernet-NIC-Geräts auf dem virtuellen Computer ähnelt dem eines beliebigen anderen Geräts, wie im Dienst für die [**Verwaltung des virtuellen Systems**](virtual-system-management-service.md)beschrieben. Die [**MSVM \_ emuatedethernetport**](msvm-emulatedethernetport.md) -und [**MSVM \_ syntheticethernetport**](msvm-syntheticethernetport.md) -Klassen stellen das virtuelle NIC-Gerät dar und werden über eine zugeordnete [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) (rasd)-Instanz konfiguriert. Das einzige ungewöhnliche Merkmal dieser Darstellung ist, dass, wenn der virtuelle Computer instanziiert wird und wiederum die **MSVM- \_ emulatedethernetport** -und **MSVM-Geräte \_ syntheticethernetport** erstellt, auch eine zugeordnete [**MSVM- \_ lanendpoint**](msvm-lanendpoint.md) -Instanz für die virtuelle NIC erstellt wird. Ebenso, wenn die virtuelle Maschine gespeichert oder ausgeschaltet wird und die Instanzen **MSVM \_ emuatedethernetport** und **MSVM \_ syntheticethernetport** zerstört werden, wird auch die zugehörige [**MSVM \_ vmlanendpoint**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) -Instanz zerstört. Der Zweck von **MSVM \_ lanendpoint** besteht darin, eine Brücke zum Verbinden von zwei Netzwerkports untereinander zu bieten. In diesem Fall wird Sie verwendet, um eine virtuelle NIC mit einem Port auf dem virtuellen switchgerät zu verbinden. Das heißt, dass die **MSVM-Instanzen " \_ emuatedethernetport** " und " **MSVM \_** " auf dem virtuellen Computer mit einer bestimmten [**MSVM \_ -**](msvm-ethernetswitchport.md) Instanz des virtuellen Switches auf dem virtuellen Computer verbunden sind. Zum Verbinden eines Schalters mit der Außenseite müssen Sie den physischen Ethernet-Port über [**bindexternalethernetport**](https://www.bing.com/search?q=**BindExternalEthernetPort**)an den [**MSVM \_ virtualswitch**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) binden. Wenn Sie einen Switch mit dem Host Netzwerk Stapel oder der internen NIC verbinden, verwenden Sie "connectinternal", damit ein virtueller Computer mit dem Host und nicht mit der Außenwelt kommuniziert. [**MSVM \_ ActiveConnection**](msvm-activeconnection.md) verbindet einen Switchport mit dem [**MSVM \_ switchlanendpoint**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) , an den der Port innerhalb von Hyper-V angeschlossen ist. Das vorhanden sein dieses Objekts bedeutet, dass der **Switchport und der MSVM \_ switchlanendpoint** aktiv verbunden sind und der Ethernet-Port, der **MSVM \_ lanendpoint** zugeordnet ist, über den Switchport mit dem Netzwerk kommunizieren kann.

 

 



