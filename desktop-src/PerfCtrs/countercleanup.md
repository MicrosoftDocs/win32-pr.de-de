---
description: Entfernt die Anbieterregistrierung.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: fe06923849a12609b6662505df94c927c3d9dfd4aeb8bc6a42bd6a225e042ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011368"
---
# <a name="countercleanup-function"></a>CounterCleanup-Funktion

Entfernt die Registrierung des Anbieters.

## <a name="syntax"></a>Syntax


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Ihr Anbieter ruft diese Funktion auf. Die Funktion ruft die [**PerfStopProvider-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) auf, um die Registrierung des Anbieters zu entfernen.

Das [**CTRPP-Tool**](ctrpp.md) generiert diese Inlinefunktion, wenn Sie das **Argument -o** angeben. Der Name der Funktion enthält eine *Präfixzeichenfolge,* wenn Sie das **Argument -prefix** angeben (z. **B. _prefix_CounterCleanup.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 




