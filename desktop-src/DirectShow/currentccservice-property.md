---
description: Die CurrentCCService-Eigenschaft legt den aktuellen Untertiteldienst fest oder ruft diesen ab.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: CurrentCCService-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d836e852d1a144abb5422f71d0127eb9c37b8f333dce0723db2c2b3b1889ec50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075960"
---
# <a name="currentccservice-property"></a>CurrentCCService-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentCCService` -Eigenschaft legt den aktuellen Untertiteldienst fest oder ruft sie ab.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den Typ des aktivierten Untertiteldiensts angibt.

## <a name="remarks"></a>Hinweise

Die möglichen Werte dieser Eigenschaft sind:



| Wert | BESCHREIBUNG                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Kein aktueller Dienst. Dies ist der Standardwert.                       |
| 0x1   | True captioning, first field. Standarddienst.                       |
| 0x2   | Beschriftung für sekundäre Sprache, zweites Feld. Im Allgemeinen nicht verwendet. |



 

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



