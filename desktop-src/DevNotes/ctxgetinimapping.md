---
description: Bestimmt, ob sich der Terminal Server im Installationsmodus befindet (nur auf Windows-Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Ctxgetinimapping-Funktion
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
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370770"
---
# <a name="ctxgetinimapping-function"></a>Ctxgetinimapping-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden. Er kann ohne vorherige Ankündigung geändert oder ausgeblendet werden. Verwenden Sie stattdessen **verifyversioninfo**.\]

Bestimmt, ob sich der Terminal Server im Installationsmodus befindet (nur auf Windows-Terminal Server 4,0).

## <a name="syntax"></a>Syntax


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **false** zurück, wenn sich der Terminal Server im Installationsmodus befindet, **true** , wenn er sich im Ausführungs Modus befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verifyversioninfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
