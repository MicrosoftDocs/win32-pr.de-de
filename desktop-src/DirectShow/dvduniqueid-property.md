---
description: Die DVDUniqueID-Eigenschaft ruft eine vom System generierte Zahl ab, die den aktuellen Datenträger eindeutig identifiziert.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: DVDUniqueID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488a3e76c93005a55f58e631f0b166b51f036e63857df3b2e21eed6e093e55b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652903"
---
# <a name="dvduniqueid-property"></a>DVDUniqueID-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDUniqueID` -Eigenschaft ruft eine vom System generierte Zahl ab, die den aktuellen Datenträger eindeutig identifiziert.

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den aktuellen Datenträger eindeutig identifiziert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Die Id(ID)-Nummer ist nicht unbedingt eindeutig, aber für alle praktischen Zwecke eindeutig. Die ID gilt für alle replizierten Kopien eines Datenträgers. Anders ausgedrückt: Alle Kopien eines bestimmten Films haben die gleiche ID. Die ID basiert auf Dateigrößen, Datumsangaben und anderen Informationen und nicht auf dem BCA-Wert.

 

 



