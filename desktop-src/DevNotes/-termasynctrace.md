---
description: Beendet die Ablauf Verfolgung.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: Termasynctrace-Funktion
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
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360985"
---
# <a name="termasynctrace-function"></a>Termasynctrace-Funktion

Beendet die Ablauf Verfolgung.

## <a name="syntax"></a>Syntax


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
