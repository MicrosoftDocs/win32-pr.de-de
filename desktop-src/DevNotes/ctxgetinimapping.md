---
description: Bestimmt, ob sich der Terminalserver im INSTALLATIONS-Modus befindet (nur Windows-Terminal Server 4.0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654210"
---
# <a name="ctxgetinimapping-function"></a>CtxGetIniMapping-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden. Es kann sich ohne vorherige Ankündigung ändern oder vollständig verschwinden. Verwenden Sie stattdessen **VerifyVersionInfo.**\]

Bestimmt, ob sich der Terminalserver im INSTALLATIONS-Modus befindet (nur Windows-Terminal Server 4.0).

## <a name="syntax"></a>Syntax


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **FALSE zurück,** wenn sich der Terminalserver im INSTALLATIONS-Modus befindet, **TRUE,** wenn er sich im EXECUTE-Modus befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
