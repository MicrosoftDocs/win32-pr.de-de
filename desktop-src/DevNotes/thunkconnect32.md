---
description: Die ThunkConnect32-Funktion wird von 16-Bit-Gerätetreibern (für MS-DOS) verwendet, die den 32-Bit-Kernel aufzurufen.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367550"
---
# <a name="thunkconnect32-function"></a>ThunkConnect32-Funktion

\[Diese Funktion wurde aus Gründen der Abwärtskompatibilität unterstützt, ist jedoch in den aktuellen Versionen von Windows nicht vorhanden. Neue Gerätetreiber sollten 32-oder 64-Bit sein und benötigen diese Funktion nicht.\]

Die **ThunkConnect32** -Funktion wird von 16-Bit-Gerätetreibern (für MS-DOS) verwendet, die den 32-Bit-Kernel aufzurufen.

## <a name="syntax"></a>Syntax


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pszDll16* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pszDll32* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*hInstance* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*dwReason* 
</dt> <dd>

Ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




