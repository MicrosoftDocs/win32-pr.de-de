---
description: Der hcrypthash-Datentyp wird verwendet, um Handles für Hash Objekte darzustellen.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: Hcrypthash (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867412"
---
# <a name="hcrypthash"></a>Hcrypthash

Der **hcrypthash** -Datentyp wird verwendet, um Handles für [*Hash Objekte*](../secgloss/h-gly.md)darzustellen. Diese Handles geben dem CSP-Modul an, welcher Hash in einem bestimmten Vorgang verwendet wird. Das CSP-Modul ermöglicht keine direkte Bearbeitung der Hashwerte. Stattdessen manipuliert der Benutzer die Hashwerte durch das Hashhandle.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 
