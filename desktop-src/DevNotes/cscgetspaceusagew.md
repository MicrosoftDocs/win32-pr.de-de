---
description: Ruft Informationen über den vom Offlinedateien Cache verwendeten Speicherplatz ab.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Cscgetspaceusagew-Funktion
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
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369189"
---
# <a name="cscgetspaceusagew-function"></a>Cscgetspaceusagew-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Ruft Informationen über den vom Offlinedateien Cache verwendeten Speicherplatz ab.

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

*lptzlocation* \[ in, out\]
</dt> <dd>

Der Verzeichnis Speicherort des Caches.

</dd> <dt>

*dwSize* \[ in\]
</dt> <dd>

Die Größe des *lptzlocation* -Puffers in Zeichen.

</dd> <dt>

*lpdwmaxspacehigh* \[ in, out\]
</dt> <dd>

Das höchst wertige **DWORD** -Wert der maximalen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpdwmaxspacelow* \[ in, out\]
</dt> <dd>

Das **DWORD** in niedriger Reihenfolge mit der maximalen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpdwcurrentspacehigh* \[ in, out\]
</dt> <dd>

Das höchst wertige **DWORD** der aktuellen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpdwcurrentspacelow* \[ in, out\]
</dt> <dd>

Das **DWORD** mit niedriger Ordnung der aktuellen Anzahl von Bytes, die im Cache verfügbar sind.

</dd> <dt>

*lpcnttotalfiles* \[ in, out\]
</dt> <dd>

Die Gesamtanzahl der Dateien im Cache.

</dd> <dt>

*lpcnttotaldirs* \[ in, out\]
</dt> <dd>

Die Gesamtanzahl der Verzeichnisse im Cache.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
