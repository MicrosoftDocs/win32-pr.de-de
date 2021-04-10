---
description: Die currentccservice-Eigenschaft legt den aktuellen Untertitel Dienst fest oder ruft ihn ab.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Currentccservice (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860346"
---
# <a name="currentccservice-property"></a>Currentccservice (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `CurrentCCService` Eigenschaft legt den aktuellen Untertitel Dienst fest oder ruft ihn ab.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den Typ des aktivierten Dienstanbieter dienstanens

## <a name="remarks"></a>Bemerkungen

Mögliche Werte für diese Eigenschaft:



| Wert | BESCHREIBUNG                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Kein aktueller Dienst. Dies ist der Standardwert.                       |
| 0x1   | True Untertitel, erstes Feld. Standard Dienst.                       |
| 0x2   | Untertitel für sekundäre Sprache, zweites Feld. Wird in der Regel nicht verwendet. |



 

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccactive**](ccactive-property.md)
</dt> </dl>

 

 



