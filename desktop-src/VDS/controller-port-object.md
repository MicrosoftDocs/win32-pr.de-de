---
description: Controller Port Objekt
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Controller Port Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343276"
---
# <a name="controller-port-object"></a>Controller Port Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Controller Port Objekt modelliert einen Controller Anschluss in einem Subsystem. Host Computer können mithilfe von Controller Anschlüssen in LUNs schreiben und daraus lesen. Controller Anschlüsse sind in Controllern in einem Subsystem enthalten. In VDS 1,1 und VDS 2.0 ist jede Controller-Ports eines Subsystems entweder auf "aktiv" oder "inaktiv" festgelegt, und zwar in Bezug auf die einzelnen LUNs des Subsystems. Ein einzelner Controllerport kann dann gleichzeitig für eine LUN auf aktiv festgelegt und für andere Benutzer inaktiv sein. Ein Controllerport, der für eine bestimmte LUN aktiv ist, ist für die Behandlung von Eingaben und Ausgaben von der LUN verantwortlich.

Aktive Controllerports dienen als einer der Endpunkte von MPIO-Pfaden in Fibre Channel Hardwareanbietern, auf denen Richtlinien für den Lastenausgleich festgelegt werden können.

Verwenden Sie die [**ivdscontrollercontrollerport:: querycontrollerports**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) -Methode, um die Controller Anschlüsse zu ermitteln, die in einem bestimmten Controller enthalten sind. Aufrufer können einen Zeiger auf einen bestimmten Controllerport abrufen, indem Sie das gewünschte Controller Port Objekt aus der-Enumeration auswählen, die von der **querycontrollerports** -Methode zurückgegeben wird. Bei einem Controller Objekt kann ein Aufrufer den Status des Controller Ports festlegen und die zugehörigen LUNs Abfragen.

Zu den Controller Objekteigenschaften gehören ein Objekt Bezeichner, ein Name, eine Seriennummer und der Status des Controller Ports.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                              | Element                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer in VDS 1,1 und 2,0 Fibre Channel Anbietern verfügbar gemacht werden | [**Ivdscontrollerport**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| Zugehörige Enumerationen                                                                           | [**VDS- \_ Port \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| Zugeordnete Strukturen                                                                             | [**VDS \_ Port \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) -und [ **VDS- \_ Port \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdscontrollercontrollerport:: querycontrollerports**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
