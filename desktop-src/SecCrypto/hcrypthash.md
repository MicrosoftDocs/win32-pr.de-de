---
description: Der HCRYPTHASH-Datentyp wird verwendet, um Handles für Hashobjekte darzustellen.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b2d20d7aeb46adda162f8d5ec380143164690bad8ee88139f9653753f1e290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006558"
---
# <a name="hcrypthash"></a>HCRYPTHASH

Der **HCRYPTHASH-Datentyp** wird verwendet, um Handles für [*Hashobjekte*](../secgloss/h-gly.md)darzustellen. Diese Handles geben dem CSP-Modul an, welcher Hash in einem bestimmten Vorgang verwendet wird. Das CSP-Modul ermöglicht keine direkte Bearbeitung der Hashwerte. Stattdessen bearbeitet der Benutzer die Hashwerte über das Hashhandle.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
