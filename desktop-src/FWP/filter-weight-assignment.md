---
title: Filtergewichtungszuweisung
description: Jeder Filter in der Windows Filterplattform (WFP) verfügt über eine zugeordnete Gewichtung, die bei der Filterausnahme verwendet wird.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9042b15da0df5f81c71a32deb923369a54243854e86aeaed1ba30c7fc8484193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746870"
---
# <a name="filter-weight-assignment"></a>Filtergewichtungszuweisung

Jeder Filter in der Windows Filterplattform (WFP) verfügt über eine zugeordnete Gewichtung, die bei der Filterausnahme [verwendet wird.](filter-arbitration.md)

Die von der Basisfilter-Engine (Base Filtering Engine, BFE) verwendete Filtergewichtung ist vom [**Typ FWP \_ UINT64.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) Aufrufer haben drei Optionen beim Hinzufügen von Filtern.

-   Legen Sie die Gewichtung auf [**einen \_ FWP-UINT64 fest.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) BFE verwendet die bereitgestellte Gewichtung wie berent.
-   Legen Sie die Gewichtung auf [**FWP \_ EMPTY fest.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) BFE generiert automatisch eine Gewichtung im Bereich \[ 0, 2⁶⁰).
-   Legen Sie die Gewichtung auf [**einen \_ FWP-UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) im Bereich \[ 0, 15 \] fest. BFE verwendet die angegebene Gewichtung als Gewichtungsbereichsbezeichner.

    BFE generiert automatisch die niedrigwertigen 60 Bits (genau so, als ob die Gewichtung auf [**FWP \_ EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)festgelegt worden wäre) und verwendet dann den angegebenen Wert, um die vier hochwertigen Bits zu setzen. Dadurch können Aufrufer den Gewichtungsbereich manuell in 16 Bereiche unterteilen und gleichzeitig die automatische Gewichtung innerhalb eines Bereichs verwenden.

> [!Note]  
> Wenn mindestens zwei Aufrufe in derselben Unterschicht registriert werden, können Probleme auftreten, wenn den Filtern die gleiche Gewichtung zugewiesen wird. Dieses Problem kann verhindert werden, indem Aufrufe ihre eigene Unterschicht mithilfe von [**FwpmSubLayerAdd0 erstellen.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Filtergewichtungsbezeichner**](filter-weight-identifiers.md)
</dt> </dl>

 

 




