---
description: Die dvduniqueid-Eigenschaft ruft eine vom systemgenerierte Zahl ab, die die aktuelle Festplatte eindeutig identifiziert.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Dvduniqueid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860278"
---
# <a name="dvduniqueid-property"></a>Dvduniqueid (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDUniqueID` -Eigenschaft ruft eine vom systemgenerierte Zahl ab, die die aktuelle Festplatte eindeutig identifiziert.

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die aktuelle Festplatte eindeutig identifiziert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Die ID-Nummer (ID) ist nicht absolut eindeutig, aber Sie ist für alle praktischen Zwecke eindeutig. Die ID gilt für alle replizierten Kopien eines Datenträgers. Anders ausgedrückt: alle Kopien eines bestimmten Films haben die gleiche ID. Die ID basiert auf Dateigrößen, Datumsangaben und anderen Informationen, nicht auf dem Wert der BCA.

 

 



