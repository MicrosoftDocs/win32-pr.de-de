---
description: Das ReadyStateChange-Ereignis wird gesendet, wenn sich die ReadyState-Eigenschaft des MSWebDVD-Steuerelements geändert hat.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f73e0b5b7cd7178df31b3f6efda56e398d8cb406598355a3c49702714686af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697120"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das `ReadyStateChange` Ereignis wird gesendet, wenn sich die **ReadyState-Eigenschaft** des MSWebDVD-Steuerelements geändert hat.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*Readystate*
</dt> <dd>

Gibt den neuen Wert der [**ReadyState-Eigenschaft**](readystate-property.md) an.



| Wert | Beschreibung               |
|-------|---------------------------|
| 0     | READYSTATE \_ UNINITIALIZED |
| 1     | READYSTATE \_ LOADING       |
| 2     | READYSTATE \_ LOADED        |
| 3     | READYSTATE \_ INTERACTIVE   |
| 4     | READYSTATE \_ COMPLETE      |



 

</dd> </dl>

 

 



