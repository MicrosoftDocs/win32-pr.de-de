---
description: Volume- und LUN-Bindung
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Volume- und LUN-Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218908"
---
# <a name="volume-and-lun-binding"></a>Volume- und LUN-Bindung

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Die Bindung ist die Erstellung von Volumes oder LUNs. Volumes bestehen aus Datenträger Blöcken und LUNs bestehen aus Laufwerks Blöcken. Die Bindung wählt für einen Satz von Zuordnungen zu physischen Ressourcen aus und erfolgt innerhalb eines Subsystems, innerhalb eines Pakets oder in beiden. Alle Anbieter Programme unterstützen eine teilweise gesteuerte Bindung eines Modells, bei dem der Aufrufer nur die Bindungs Attribute eines bestimmten Interesses angibt und es dem Anbieter ermöglicht, den Rest auszuwählen. Die Vorgänge in VDS für das Binden von Volumes und LUNs sind ähnlich, aber nicht identisch. Hardware Anbieter können z. b. zusätzliche Bindungs Optionen anbieten.

VDS unterstützt die folgenden fünf Volume-und LUN-Bindungs Typen für teilweise gesteuerte Konfigurationen. (Hardware Anbieter können viele andere Bindungen unterstützen und unterstützen.)



| Begriff                                                                                                                                             | BESCHREIBUNG                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Einfache<br/>                                                     | Lineare Zuordnung mit nur einem zusammenhängenden Block.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Übergreifende<br/>                                                 | Lineare Zuordnung mit mehreren nicht zusammenhängenden Blöcken auf mehreren Datenträgern oder Laufwerken.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Tem<br/>                                                 | Eine Zuordnung, die zusammenhängende volumeblöcke auf mehrere Datenträger oder Laufwerke erweitert.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Verkehrt<br/>                                             | Zuordnung, die zwei oder mehr identische Datenkopien verwaltet.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Stripeset mit Parität<br/> | Zuordnung, mit der Paritäts Überprüfung-Informationen auf mehrere Datenträger oder Laufwerke verteilt werden.<br/>  |



 

VDS erstellt gespiegelte, Stripesets und Stripesets mit Paritäts Bindungen von mehr als einem Element. Beispielsweise hat eine zwei-Wege-Spiegelung zwei Member. Jedes Mitglied kann Blöcke auf mehr als einem Datenträger oder Laufwerk belegen. VDS verkettet die Blöcke, um den Member zu bilden, und bindet dann das Volume oder die LUN an die Elemente. Ein Anbieter kann alle Bindungs Typen oder eine beliebige Teilmenge unterstützen. Im VDS-Objektmodell ist jedes Mitglied einer Spiegelung ein unabhängiges Objekt, das als Plex bezeichnet wird.

Auch hier sind Volume-und LUN-Typen ähnlich, aber nicht exakt. Eine Beschreibung der Volumetypen finden Sie im [Volume-Objekt](volume-object.md). Informationen zu LUN-Typen finden Sie unter dem [LUN-Objekt](lun-object.md). Bindungs Typen sind entweder nicht fehlertolerant oder fehlertolerant.

### <a name="non-fault-tolerant-binding"></a>Nicht fehlertolerante Bindung

Nicht fehlertolerante Volumes und LUNs bieten keine Notfall Wiederherstellung. Wenn eines der Spindeln, das zu einem nicht fehlertoleranten Volume oder einer LUN beiträgt, fehlschlägt, schlägt das gesamte Volume oder die LUN fehl. In Exchange für das Risiko von Daten bieten nicht fehlertolerante Volumes und LUNs eine Eingabe-/Ausgabeleistung, die in der Regel der von fehlertoleranten Volumes und LUNs entspricht. VDS unterstützt die folgenden drei nicht fehlertoleranten Typen: einfache, übergreifende und stripesettypen.

Einfach

![Diagramm, das einen einfachen nicht fehlertoleranten Typ mit 2 Paketen und 2 Subsystemen anzeigt.](images/vdssimplelunvol.png)

Übergreifend

![Diagramm, das einen übergreifenden, nicht fehlertoleranten Typ mit 1 Pack und 1 Subsystem anzeigt.](images/vdsspanlunvol.png)

Tem

![Diagramm, das einen nicht fehlertoleranten Datenträger mit 1 Pack und 1 Subsystem anzeigt.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Fehlertolerante Bindung

Die folgenden fehlertoleranten Volumes und LUNs bieten eine Notfall Wiederherstellung. Wenn eines der Spindeln, das zu einem fehlertoleranten Volume oder einer LUN beiträgt, fehlschlägt, können die Daten wieder hergestellt werden. In Exchange für die Datensicherheit ist die Eingabe-/Ausgabeleistung von fehlertoleranten Volumes und LUNs in der Regel geringer als bei nicht fehlertoleranten Volumes und LUNs. VDS unterstützt zwei fehlertolerante Typen: gespiegelt und Stripeset mit Parität.

Gespiegelt (drei-Wege-Spiegelung)

![Diagramm, das einen gespiegelten (3-Wege-Spiegel) fehlertoleranten Typ anzeigt.](images/vdsmirrorlunvol.png)

Stripeset mit Parität

![Diagramm, das ein Stripeset mit einem Paritäts fehlertoleranten Typ anzeigt](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurations Übersicht](configuration.md)
</dt> <dt>

[Volume-Objekt](volume-object.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> </dl>

 

