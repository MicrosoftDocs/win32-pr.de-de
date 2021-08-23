---
description: Initialisiert die IME-Freigabe.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 178b39c67d12473663eb93bc300651341a9c459c19680218fa2c6f7a939c688c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691380"
---
# <a name="finitimeshare-function"></a>FInitIMEShare-Funktion

Initialisiert die IME-Freigabe.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE** bei Erfolg zurück, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

Diese Funktion sollte aufgerufen werden, bevor andere IME-Freigabefunktionen aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EndIMEShare**](endimeshare.md)
</dt> </dl>

 

 
