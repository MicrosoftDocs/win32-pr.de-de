---
description: Beendet die IME-Freigabe.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: Endimeshare-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352822"
---
# <a name="endimeshare-function"></a>Endimeshare-Funktion

Beendet die IME-Freigabe.

## <a name="syntax"></a>Syntax


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

Diese Funktion sollte aufgerufen werden, nachdem die letzte IME-Freigabe Funktion aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Finitimeshare**](finitimeshare.md)
</dt> </dl>

 

 
