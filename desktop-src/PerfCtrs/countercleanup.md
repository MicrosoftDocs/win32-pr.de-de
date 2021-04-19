---
description: Entfernt die Anbieter Registrierung.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Countercleanup-Funktion
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
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368749"
---
# <a name="countercleanup-function"></a>Countercleanup-Funktion

Entfernt die Anbieter Registrierung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Anbieter ruft diese Funktion auf. Die-Funktion Ruft die [**perfstopprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) -Funktion auf, um die Registrierung des Anbieters zu entfernen.

Das [**ctrpp**](ctrpp.md) -Tool generiert diese Inline Funktion, wenn Sie das **-o-** Argument angeben. Der Name der Funktion enthält eine *Präfix* Zeichenfolge, wenn Sie das Argument **-prefix** angeben (z. b. **_prefix_CounterCleanup**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 




