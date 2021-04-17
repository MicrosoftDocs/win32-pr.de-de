---
description: Das Ereignis "Read ystatechange" wird gesendet, wenn sich die Eigenschaft "Read-State" des mswebdvd-Steuer Elements geändert hat.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: "\"Leserystatechange\""
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522048"
---
# <a name="readystatechange"></a>"Leserystatechange"

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das `ReadyStateChange` Ereignis wird gesendet, wenn die Eigenschaft "read- **State** " des mswebdvd-Steuer Elements geändert wurde.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*
</dt> <dd>

Gibt den neuen Wert der Eigenschaft " [**leserystate**](readystate-property.md) " an.



| Wert | BESCHREIBUNG               |
|-------|---------------------------|
| 0     | "Read ystate" ist \_ nicht initialisiert. |
| 1     | Laden von "Read ystate" \_       |
| 2     | "Read ystate" \_ geladen        |
| 3     | Read-State \_ interaktiv   |
| 4     | Read-State ist fertiggestellt. \_      |



 

</dd> </dl>

 

 



