---
description: Die EnableResetOnStop-Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der bestimmt, wie die Wiedergabe fortgesetzt wird, wenn das Filterdiagramm einen Übergang von einem angehaltenen Zustand vornimmt.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: EnableResetOnStop-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4bfda62839f55dcb4c4597fdad6654072f4dfeb2450c3bce3ed99c13a418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107860"
---
# <a name="enableresetonstop-property"></a>EnableResetOnStop-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `EnableResetOnStop` -Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der bestimmt, wie die Wiedergabe fortgesetzt wird, wenn das Filterdiagramm einen Übergang von einem angehaltenen Zustand vornimmt.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, wo das MSWebDVD-Objekt wieder wiedergegeben wird, nachdem das Filterdiagramm beendet wurde.

## <a name="remarks"></a>Hinweise

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

Die möglichen Werte dieser Eigenschaft sind: mit dem Standardwert true.



| Wert | BESCHREIBUNG                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | DER DVD-Navigator wird zurückgesetzt und beginnt mit der Wiedergabe am Anfang des Datenträgers. Dies ist der Standardwert. |
| false | Der DVD-Navigator setzt die Wiedergabe dort fort, wo er aufgehört hat.                                                 |



 

 

 



