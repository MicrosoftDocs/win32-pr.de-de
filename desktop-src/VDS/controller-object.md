---
description: Controller Objekt
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Controller Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104568072"
---
# <a name="controller-object"></a>Controller Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Controller Objekt modelliert einen Controller in einem Subsystem. Controller sind in Subsystemen enthalten, und jeder Controller verfügt über einen oder mehrere Controllerports, über die der Host Computer in LUNs schreiben und aus diesen lesen kann. Ein einzelner Controller kann gleichzeitig für eine LUN auf aktiv festgelegt und für andere Benutzer inaktiv sein. Ein Controller, der für eine angegebene LUN aktiv ist, ist für die Behandlung von Eingaben und Ausgaben von der LUN verantwortlich. Diese Idee wird in der folgenden Abbildung veranschaulicht.

![Diagramm, das einen "controller" mit einer aktiven LUN auf der linken Seite und zwei aktive LUNs auf der rechten Seite anzeigt.](images/vdscontroller.png)

**VDS 1,0:** Alle Controller eines Subsystems sind entweder auf "aktiv" oder "inaktiv" festgelegt, und zwar in Bezug auf die einzelnen LUNs, die das Subsystem hat.

VDS-Anwendungen verwenden die [**ivdssubsystem:: querycontrollers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) -Methode, um die Controller zu ermitteln, die in einem bestimmten Subsystem enthalten sind. Aufrufer können einen Zeiger auf einen bestimmten Controller abrufen, indem Sie das gewünschte Controller Objekt aus der-Enumeration auswählen, die von der **querycontrollers** -Methode zurückgegeben wird. Mit einem Controller Objekt kann ein Aufrufer den Controller Status festlegen, die zugehörigen LUNs Abfragen, seine Controller Anschlüsse Abfragen und den Cache leeren und für ungültig erklären.

Zusätzlich zu einem Objekt Bezeichner, einem Namen und einer Seriennummer enthalten die Eigenschaften des Controller Objekts den Controller Status und-Zustand sowie die Anzahl der Ports.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                              | Element                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden                                                 | [**Ivdscontroller**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| Schnittstellen, die von diesem Objekt immer in VDS 1,1 und 2,0 Fibre Channel Anbietern verfügbar gemacht werden | [**Ivdscontrollercontrollerport**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können                                                     | [**Ivdsmaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| Zugehörige Enumerationen                                                                           | [**VDS \_ Controller \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).                                                                      |
| Zugeordnete Strukturen                                                                             | [**VDS \_ Controller- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) -und [**VDS- \_ Controller \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdssubsystem:: querycontrollers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
