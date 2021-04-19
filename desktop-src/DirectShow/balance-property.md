---
description: Die Balance-Eigenschaft legt den Lautsprecher Saldo für die audiostreamausgabe fest oder ruft ihn ab.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Balance (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345410"
---
# <a name="balance-property"></a>Balance (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Balance` -Eigenschaft legt den Referenten Saldo für die audiostreamausgabe fest oder ruft ihn ab.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Ausgleichs Ebenen darstellt. Der zulässige Eingabebereich ist-10.000 bis 10.000. Bei einem Wert von 0 wird ein neutrales Gleichgewicht festgelegt, d. h., der linke und der Rechte Sprecher erhalten dasselbe Amplitude-Audiosignal.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff mit einem Standardwert von 0. Dies bedeutet, dass beide Redner äquivalente Audiosignale erhalten. Wie bei der [**Volume**](volume-property.md) -Eigenschaft entsprechen Einheiten 01 Dezibel (multipliziert mit-1, wenn


```
iBalance
```



ist ein positiver Wert). Der Wert 1000 gibt z. b. 10 dB auf dem rechten Kanal und 90 dB im linken Kanal an.

 

 



