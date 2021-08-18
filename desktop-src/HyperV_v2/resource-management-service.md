---
description: Das Ressourcenvirtualisierungsprofil bietet die Möglichkeit, mit der ein Client die vom Virtualisierungssystem unterstützten virtuellen Ressourcen ermitteln kann.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Ressourcenverwaltungsdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593af3c440ad15add50445a3b05f41d44c8c396a1334635aeaf141838e82e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746215"
---
# <a name="resource-management-service"></a>Ressourcenverwaltungsdienst

Das Ressourcenvirtualisierungsprofil bietet die Möglichkeit, mit der ein Client die vom Virtualisierungssystem unterstützten virtuellen Ressourcen ermitteln kann. Außerdem wird die Kapazität oder Anzahl von Zuordnungen beschrieben, die für jeden Typ virtueller Ressourcen unterstützt wird. Die folgende Abbildung zeigt das Ressourcenvirtualisierungsprofil.

![Ressourcenvirtualisierungsprofil](images/resourcemanagement.png)

Das Ressourcenvirtualisierungsprofil definiert zwei verschiedene Klassen virtueller Ressourcen:

-   Freigegebene Ressource: Stellt die Ressourcen des Hosts dar, die von mehreren virtuellen Computern gemeinsam genutzt werden können. [**Msvm \_ Der Prozessor**](msvm-processor.md) ist ein Beispiel für eine freigegebene Ressource.
-   Synthetische Ressource: Stellt die virtuellen Ressourcen dar, die über keine entsprechende Hostressource verfügen. [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) ist ein Beispiel für eine synthetische Ressource.

Der Ressourcenpool wird verwendet, um eine Klasse von Hostressourcen zu erfassen, sodass er leicht ermittelt werden kann, während seine Funktionen und Einstellungen an einem zentralen Ort beschrieben werden können. Es gibt keine Beschränkung dafür, wie einfach oder erweitert eine Implementierung der gesammelten Ressource sein kann.

Über den Ressourcenpool kann der Client auf die zugeordneten Zuordnungsfunktionen (Allocation Capabilities, AC) zugreifen. Diese Klasse beschreibt die Funktionen der Ressource, die von diesem Ressourcenpool beschrieben wird. Beispielsweise kann es angeben, ob der von diesem Ressourcenpool [**dargestellte Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) virtuelle LANs (VLANs) oder Filter unterstützt.

Das AC-Profil definiert die Mittel, mit denen ein Client den gültigen Bereich von und die Standardeinstellungen für eine bestimmte virtuelle Ressource ermitteln kann. Jedem Ressourcenpool ist ein AC-Objekt zugeordnet. Dem AC-Objekt sind vier RASD-Objekte (Resource Allocation Setting Data) zugeordnet, um die Minimal-, Höchst-, Standard- und inkrementellen Werte für die Zuordnung der jeweiligen Ressource zu beschreiben. Zusammen beschreiben diese Klassen den gesamten Bereich der unterstützten Funktionen. Die [**Msvm \_ AllocationCapabilities-Instanz**](msvm-allocationcapabilities.md) stellt einen Ankerpunkt für den Satz von [**Msvm \_ ResourceAllocationSettingData-Instanzen**](msvm-resourceallocationsettingdata.md) bereit, die den Standard- und gültigen Einstellungsbereich für eine virtuelle Ressource angeben. Die [**Msvm \_ SettingsDefineCapabilities-Zuordnungsklasse**](msvm-settingsdefinecapabilities.md) stellt die Verknüpfung zwischen der AC-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine Ressource bereit, die von der Virtualisierungsplattform unterstützt wird.

 

 



