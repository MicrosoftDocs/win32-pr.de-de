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
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888580"
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