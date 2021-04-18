---
description: Initialisiert die IME-Freigabe.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Finitimeshare-Funktion
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
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365513"
---
# <a name="finitimeshare-function"></a>Finitimeshare-Funktion

Initialisiert die IME-Freigabe.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Andernfalls gibt die Funktion **true** bei Success oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

Diese Funktion sollte aufgerufen werden, bevor andere IME-Freigabe Funktionen aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Umdimeshare**](endimeshare.md)
</dt> </dl>

 

 
