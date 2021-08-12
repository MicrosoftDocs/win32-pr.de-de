---
description: Beendet die Ablaufverfolgung.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: TermAsyncTrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 6857e8e6164392a12604779d51914d7d297ec89a3890adec000cf662019a7485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668799"
---
# <a name="termasynctrace-function"></a>TermAsyncTrace-Funktion

Beendet die Ablaufverfolgung.

## <a name="syntax"></a>Syntax


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich ist. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
