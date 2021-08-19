---
description: Bestimmt den Speicherort einer Ressource mit dem angegebenen Typ und Namen im angegebenen Modul.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bfd640aaf0bbc68e8798f62f41542d794db34808674c0bdb47587c7396ad7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094195"
---
# <a name="findresourcewrapw-function"></a>FindResourceWrapW-Funktion

\[**FindResourceWrapW** ist für die Verwendung in Windows XP verfügbar. In nachfolgenden Versionen ist sie möglicherweise nicht verfügbar. Verwenden Sie stattdessen [**FindResourceW.**](/windows/win32/api/winbase/nf-winbase-findresourcea)\]

Bestimmt den Speicherort einer Ressource mit dem angegebenen Typ und Namen im angegebenen Modul.

> [!Note]  
> **FindResourceWrapW** ist ein Wrapper für die **FindResourceW-Funktion.** Weitere Nutzungshinweise finden Sie unter [**FindResource.**](/windows/win32/api/winbase/nf-winbase-findresourcea)

 

## <a name="syntax"></a>Syntax


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hModule* \[ In\]
</dt> <dd>

Typ: **HMODULE**

Ein Handle für das Modul, dessen ausführbare Datei die Ressource enthält. Der Wert **NULL** gibt das Modulhandle an, das der Imagedatei zugeordnet ist, die das Betriebssystem zum Erstellen des aktuellen Prozesses verwendet hat.

</dd> <dt>

*lpName* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Der Name der Ressource. Weitere Informationen finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lpType* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die den Ressourcentyp angibt. Weitere Informationen finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRSRC**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für den Informationsblock der angegebenen Ressource. Um ein Handle für die Ressource abzurufen, übergeben Sie dieses Handle an die [**LoadResource-Funktion.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)

Wenn die Funktion fehlschlägt, ist der Rückgabewert **NULL.** Um erweiterte Fehlerinformationen abzurufen, rufen Sie die [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Hinweise

Wenn Sie eine bestimmte Lokalisierung angeben müssen, verwenden Sie die [**FindResourceEx-Funktion**](/windows/win32/api/winbase/nf-winbase-findresourceexa) anstelle von **FindResourceWrapW.**

**FindResourceWrapW** bietet die Möglichkeit, Unicode-Zeichenfolgen in älteren Betriebssystemen zu verwenden. Die bevorzugte Methode ist die Verwendung von [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in Verbindung mit Microsoft Layer for Unicode (MSLU).

**FindResourceWrapW** muss direkt über Shlwapi.dll aufgerufen werden, wobei Ordinalzahl 66 verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Findresource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
