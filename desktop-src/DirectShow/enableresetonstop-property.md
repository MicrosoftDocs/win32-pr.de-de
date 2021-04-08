---
description: Die enableresetonstopp-Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der bestimmt, wie die Wiedergabe fortgesetzt wird, wenn das Filter Diagramm einen Übergang von einem beendeten Zustand bewirkt.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Enableresetonstoppt (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746648"
---
# <a name="enableresetonstop-property"></a>Enableresetonstoppt (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `EnableResetOnStop` Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der bestimmt, wie die Wiedergabe fortgesetzt wird, wenn das Filter Diagramm einen Übergang vom beendeten Zustand bewirkt.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, wo das mswebdvd-Objekt wieder abgespielt wird, nachdem das Filter Diagramm angehalten wurde.

## <a name="remarks"></a>Bemerkungen

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

Mögliche Werte für diese Eigenschaft sind: mit dem Standardwert true.



| Wert | BESCHREIBUNG                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | Der DVD-Navigator wird zurückgesetzt und startet am Anfang der Festplatte. Dies ist der Standardwert. |
| false | Der DVD-Navigator wird wiedergegeben, wo er aufgehört hat.                                                 |



 

 

 



