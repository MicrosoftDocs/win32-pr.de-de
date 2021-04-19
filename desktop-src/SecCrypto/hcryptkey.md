---
description: Der hcryptkey-Datentyp wird verwendet, um Handles für kryptografische Schlüssel darzustellen.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: Hcryptkey (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351427"
---
# <a name="hcryptkey"></a>Hcryptkey

Der **hcryptkey** -Datentyp wird verwendet, um Handles für [*kryptografische Schlüssel*](../secgloss/c-gly.md)darzustellen. Diese Handles werden verwendet, um das CSP-Modul anzugeben, welcher Schlüssel in einem bestimmten Vorgang verwendet wird. Das CSP-Modul ermöglicht keinen direkten Zugriff auf die Schlüsselwerte. Stattdessen führt der Benutzer Funktionen mithilfe des Schlüssel Werts über das Schlüssel Handle aus.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 
