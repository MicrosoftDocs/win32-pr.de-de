---
description: Das ressourcenvirtualisierungsprofil bietet die Möglichkeiten, mit denen ein Client die vom Virtualisierungssystem unterstützten virtuellen Ressourcen ermitteln kann.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Ressourcen Verwaltungsdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c405cac60df719195466da6ea0c7aadb7bf0d765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050397"
---
# <a name="resource-management-service"></a>Ressourcen Verwaltungsdienst

Das ressourcenvirtualisierungsprofil bietet die Möglichkeiten, mit denen ein Client die vom Virtualisierungssystem unterstützten virtuellen Ressourcen ermitteln kann. Außerdem wird die Kapazitäts – bzw. die Anzahl der Zuordnungen – beschrieben, die für jeden virtuellen Ressourcentyp unterstützt werden. Die folgende Abbildung zeigt das ressourcenvirtualisierungsprofil.

![ressourcenvirtualisierungsprofil](images/resourcemanagement.png)

Zwei verschiedene Klassen virtueller Ressourcen werden vom ressourcenvirtualisierungsprofil definiert:

-   Shared Resource: stellt die Ressourcen des Hosts dar, die von mehreren virtuellen Maschinen gemeinsam genutzt werden können. [**MSVM \_ Der Prozessor**](msvm-processor.md) ist ein Beispiel für eine freigegebene Ressource.
-   Synthetische Ressource: stellt die virtuellen Ressourcen dar, die keine entsprechende Host Ressource aufweisen. [**MSVM \_ Emuatedethernetport**](msvm-emulatedethernetport.md) ist ein Beispiel für eine synthetische Ressource.

Der Ressourcenpool wird verwendet, um eine Klasse von Host Ressourcen zu erfassen, damit Sie leicht erkannt werden kann, während ihre Funktionen und Einstellungen an einem zentralen Ort beschrieben werden können. Es gibt keine Beschränkung, wie einfach oder erweitert eine Implementierung der gesammelten Ressource sein kann.

Aus dem Ressourcenpool kann der Client auf die zugeordneten Zuordnungs Funktionen (AC) zugreifen. Diese Klasse beschreibt die Funktionen der Ressourcen, die von diesem Ressourcenpool beschrieben werden. So kann beispielsweise angegeben werden, ob der von diesem Ressourcenpool dargestellte [**MSVM \_ emuatedethernetport**](msvm-emulatedethernetport.md) virtuelle LANs (VLANs) oder Filter unterstützt.

Mit dem AC-Profil wird definiert, auf welche Weise ein Client den gültigen Bereich von und die Standardeinstellungen für eine bestimmte virtuelle Ressource ermitteln kann. Jedem Ressourcenpool ist ein AC-Objekt zugeordnet. Dem AC-Objekt sind vier Ressourcen Zuordnungs Einstellungsdaten (rasd) zugeordnet, um den minimalen, maximalen, standardmäßigen und inkrementellen Wert für die Zuordnung der angegebenen Ressource zu beschreiben. In dieser Klasse werden alle unterstützten Funktionen beschrieben. Die [**MSVM \_ zugsfunktionen**](msvm-allocationcapabilities.md) -Instanz stellt einen Ankerpunkt für den Satz von [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Instanzen bereit, die den standardmäßigen und gültigen Bereich von Einstellungen für eine virtuelle Ressource angeben. Die [**MSVM \_ settingsdefinecapabiliassociation**](msvm-settingsdefinecapabilities.md) -Klasse stellt die Verknüpfung zwischen der AC-Instanz und den minimalen, maximalen, inkrementellen und Standardeinstellungen für eine von der Virtualisierungsplattform unterstützte Ressource bereit.

 

 



