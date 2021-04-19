---
description: Bestimmt, ob die App die Daten aus der Systemablage pullen muss, anstatt sie aus ihrem internen Cache zu entfernen.
title: DlpMustPasteFromSystemClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495729"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>DlpMustPasteFromSystemClipboard-Funktion

Bestimmt, ob die App die Daten aus der Systemablage pullen muss, anstatt sie aus ihrem internen Cache zu entfernen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Rückgabewert

TRUE, wenn der Aufruf in der Betriebssystem-Zwischenablage obligatorisch ist; andernfalls FALSE.

## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |