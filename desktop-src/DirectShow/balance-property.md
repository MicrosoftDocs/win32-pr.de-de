---
description: Die Balance-Eigenschaft legt den Lautsprecherstand für die Audiostreamausgabe fest oder ruft sie ab.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Balance-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4faa8bcacb8c4603dcb67ee6cc617ced4b31bd7afa3afa16d3ba3831040a004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689380"
---
# <a name="balance-property"></a>Balance-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Balance` -Eigenschaft legt den Lautsprecherstand für die Audiostreamausgabe fest oder ruft sie ab.

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Saldoebenen darstellt. Der zulässige Eingabebereich ist -10.000 bis 10.000. Der Wert 0 legt einen neutralen Ausgleich fest, d.&a; sowohl linker als auch rechter Lautsprecher erhalten das gleiche Amplitudenaudiosignal.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist Lese-/Schreibzugriff mit dem Standardwert 0. Das bedeutet, dass beide Sprecher gleichwertige Audiosignale empfangen. Wie bei der [**Volume-Eigenschaft**](volume-property.md) entsprechen Einheiten 0,01 Dezibel (multipliziert mit -1, wenn


```
iBalance
```



ist ein positiver Wert). Der Wert 1000 gibt beispielsweise 10 dB im rechten Kanal und 90 dB im linken Kanal an.

 

 



