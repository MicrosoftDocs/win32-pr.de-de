---
description: Volume- und LUN-Bindung
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Volume- und LUN-Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91014241014793b601c15c64ec19e5a2b1d153c71ba617cead54a5d68cf978b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125567"
---
# <a name="volume-and-lun-binding"></a>Volume- und LUN-Bindung

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Bindung ist die Erstellung von Volumes oder LUNs. Volumes bestehen aus Datenträger-Extents und LUNs bestehen aus Laufwerksddungen. Die Bindung wählt für eine Reihe von Zuordnungen zu physischen Ressourcen aus und tritt innerhalb eines Subsystems, innerhalb eines Pakets oder in beiden Fällen auf. Alle Anbieterprogramme unterstützen die teilweise gerichtete Bindung eines Modells, bei dem der Aufrufer nur die Bindungsattribute angibt, die von besonderem Interesse sind, und dem Anbieter ermöglicht, den Rest zu wählen. Die Vorgänge in VDS für Bindungsvolumes und LUNs sind ähnlich, aber nicht identisch. Beispielsweise können Hardwareanbieter zusätzliche Bindungsoptionen anbieten.

VDS unterstützt die folgenden fünf Volume- und LUN-Bindungstypen für teilweise gerichtete Konfigurationen. (Hardwareanbieter können und unterstützen viele andere Bindungen.)



| Begriff                                                                                                                                             | BESCHREIBUNG                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Einfach<br/>                                                     | Lineare Zuordnung mit einem und nur einem zusammenhängenden Extent.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Übergreifende<br/>                                                 | Lineare Zuordnung mit mehreren nicht zusammenhängenden Speichereinheiten auf mehreren Datenträgern oder Laufwerken.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Gestreift<br/>                                                 | Zuordnung, die zusammenhängende Volume-Extents über mehrere Datenträger oder Laufwerke hinweg überlagert.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Gespiegelten<br/>                                             | Zuordnung, die zwei oder mehr identische Datenkopien verwaltet.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striping mit Parität<br/> | Zuordnung, die Paritätsüberprüfungsinformationen auf mehrere Datenträger oder Laufwerke verteilt.<br/>  |



 

VDS erstellt gespiegelte, gestreifte und gestreifte Konstrukte mit Paritätsbindungen aus mehr als einem Member. Beispielsweise verfügt eine zweigespiegelte -Spiegelung über zwei Member. Jedes Mitglied kann Aufdungen auf mehr als einem Datenträger oder Laufwerk belegen. VDS verkettet die Extent, um den Member zu bilden, und bindet dann das Volume oder die LUN an die Member. Ein Anbieter kann alle Bindungstypen oder eine beliebige Teilmenge unterstützen. Im VDS-Objektmodell ist jeder Member eines Spiegels ein unabhängiges Objekt, das als Plex bezeichnet wird.

Auch hier sind Volume- und LUN-Typen ähnlich, aber nicht genau. Eine Beschreibung der Volumetypen finden Sie im [Volume-Objekt](volume-object.md). Informationen zu LUN-Typen finden Sie im [LUN-Objekt](lun-object.md). Bindungstypen sind entweder nicht fehlertolerant oder fehlertolerant.

### <a name="non-fault-tolerant-binding"></a>Nicht fehlertolerante Bindung

Nicht fehlertolerante Volumes und LUNs bieten keine Notfallwiederherstellung. Wenn eine der Achsen, die zu einem nicht fehlertoleranten Volume oder einer nicht fehlertoleranten LUN bei tragen, ausfällt, schlägt das gesamte Volume oder die gesamte LUN fehl. Im Gegenzug für das Risiko für Daten bieten nicht fehlertolerante Volumes und LUNs eine Eingabe-/Ausgabeleistung, die im Allgemeinen der Leistung fehlertoleranter Volumes und LUNs überlegen ist. VDS unterstützt die folgenden drei nicht fehlertoleranten Typen: "simple", "spanned" und "striped".

Einfach

![Diagramm, das einen einfachen, nicht fehlertoleranten Typ mit 2 Paketen und 2 Subsystemen zeigt.](images/vdssimplelunvol.png)

Übergreifend

![Diagramm, das einen nicht fehlertoleranten übergreifenden Typ mit 1 Paket und 1 Subsystem zeigt.](images/vdsspanlunvol.png)

Gestreift

![Diagramm, das einen nicht fehlertoleranten Striped-Typ mit 1 Paket und 1 Subsystem zeigt.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Fehlertolerante Bindung

Die folgenden fehlertoleranten Volumes und LUNs bieten eine Notfallwiederherstellung. Wenn eine der Achsen, die zu einem fehlertoleranten Volume oder einer FEHLER-LUN bei tragen, ausfällt, können die Daten wiederhergestellt werden. Im Gegenzug für die Datensicherheit ist die Eingabe-/Ausgabeleistung von fehlertoleranten Volumes und LUNs im Allgemeinen mit der Leistung nicht fehlertoleranter Volumes und LUNs bzw. VDS unterstützt zwei fehlertolerante Typen: gespiegelt und mit Parität gestreift.

Gespiegelt (Drei-Wege-Spiegelung)

![Diagramm, das einen fehlertoleranten Typ gespiegelt (3-Wege-Spiegelung) zeigt.](images/vdsmirrorlunvol.png)

Striping mit Parität

![Diagramm, das einen fehlertoleranten Striped-Typ mit Parität zeigt.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Konfiguration](configuration.md)
</dt> <dt>

[Volume-Objekt](volume-object.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> </dl>

 

