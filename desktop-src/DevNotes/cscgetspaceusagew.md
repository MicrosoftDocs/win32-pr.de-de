---
description: Ruft Informationen über den vom Cache verwendeten Speicherplatz Offlinedateien ab.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667953"
---
# <a name="cscgetspaceusagew-function"></a>CSCGetSpaceUsageW-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Ruft Informationen über den vom Cache verwendeten Speicherplatz Offlinedateien ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lptzLocation* \[ in, out\]
</dt> <dd>

Der Verzeichnisspeicherort des Caches.

</dd> <dt>

*dwSize* \[ In\]
</dt> <dd>

Die Größe des *lptzLocation-Puffers* in Zeichen.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ in, out\]
</dt> <dd>

Das obere **DWORD der** maximalen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpdwMaxSpaceLow* \[ in, out\]
</dt> <dd>

Das niedrige **DWORD der** maximalen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ in, out\]
</dt> <dd>

Das obere **DWORD der** aktuellen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ in, out\]
</dt> <dd>

Das niedrige **DWORD der** aktuellen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpcntTotalFiles* \[ in, out\]
</dt> <dd>

Die Gesamtanzahl der Dateien im Cache.

</dd> <dt>

*lpcntTotalDirs* \[ in, out\]
</dt> <dd>

Die Gesamtanzahl der Verzeichnisse im Cache.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich ist. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
