---
description: Gibt an, ob der aktuelle Benutzer ein Administrator ist.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: psetupisuseradmin-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358677"
---
# <a name="psetupisuseradmin-function"></a>psetupisuseradmin-Funktion

\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]

Gibt an, ob der aktuelle Benutzer ein Administrator ist.

## <a name="syntax"></a>Syntax


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

**True** , wenn der aktuelle Benutzer ein Administrator ist, andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
