---
title: Filtergewichtungszuweisung
description: Jeder Filter in der Windows-Filter Plattform (Windows Filtering Platform, WFP) verfügt über eine zugeordnete Gewichtung, die bei der Filterung von Filtern verwendet wird.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "104390068"
---
# <a name="filter-weight-assignment"></a>Filtergewichtungszuweisung

Jeder Filter in der Windows-Filter Plattform (Windows Filtering Platform, WFP) verfügt über eine zugeordnete Gewichtung, die bei der [Filterung von Filtern](filter-arbitration.md)verwendet wird.

Die von der Basis Filter-Engine (BFE) verwendete Filter Gewichtung ist vom Typ " [**f \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)". Aufrufer haben beim Hinzufügen von Filtern drei Möglichkeiten.

-   Legen Sie die Gewichtung auf eine [**FWP- \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)fest. BFE verwendet die angegebene Gewichtung unverändert.
-   Legen Sie die Gewichtung auf [**FWP \_ leer**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)fest. BFE generiert automatisch eine Gewichtung im Bereich von \[ 0, 2 ⁶ ⁰).
-   Legen Sie die Gewichtung auf eine [**FWP- \_ Uint8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) im Bereich von \[ 0 bis 15 fest \] . BFE verwendet die angegebene Gewichtung als Gewichtungs Bereichs Bezeichner.

    BFE generiert automatisch die nieder wertigen 60 Bits (genau so, als ob die Gewichtung auf [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)festgelegt wurde), und verwendet dann den bereitgestellten Wert, um die vier hohen Bestell Bits festzulegen. Dadurch können Aufrufer den Gewichtungs Bereich manuell in 16 Bereiche aufteilen, während gleichzeitig die automatische Gewichtung innerhalb eines Bereichs verwendet wird.

> [!Note]  
> Wenn zwei oder mehr Legenden auf derselben Unterschicht registriert werden, können Probleme auftreten, wenn die gleiche Gewichtung den Filtern zugewiesen ist. Dieses Problem kann verhindert werden, indem [**Sie mithilfe von**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)"Legenden" eine eigene Unterschicht erstellen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Filtern von Gewichtungs bezeichlern**](filter-weight-identifiers.md)
</dt> </dl>

 

 




