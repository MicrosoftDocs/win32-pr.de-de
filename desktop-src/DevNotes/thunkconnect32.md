---
description: Die ThunkConnect32-Funktion wird von 16-Bit-Gerätetreibern (für MS-DOS) verwendet, die den 32-Bit-Kernel aufrufen.
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
ms.openlocfilehash: 3f754d4c0e88ee860d112a6fb99d15c2690af0014951e77425d425b65ad16e39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929110"
---
# <a name="thunkconnect32-function"></a>ThunkConnect32-Funktion

\[Diese Funktion wurde aus Gründen der Abwärtskompatibilität unterstützt, ist aber in aktuellen Versionen von nicht Windows. Neue Gerätetreiber sollten 32- oder 64-Bit sein und benötigen diese Funktion nicht.\]

Die **ThunkConnect32-Funktion** wird von 16-Bit-Gerätetreibern (für MS-DOS) verwendet, die den 32-Bit-Kernel aufrufen.

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

Gibt immer **FALSE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




