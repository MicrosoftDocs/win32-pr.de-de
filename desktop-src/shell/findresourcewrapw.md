---
description: Bestimmt den Speicherort einer Ressource mit dem angegebenen Typ und Namen im angegebenen Modul.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Findresourcewrapw-Funktion
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
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215958"
---
# <a name="findresourcewrapw-function"></a>Findresourcewrapw-Funktion

\[**Findresourcewrapw** ist für die Verwendung in Windows XP verfügbar. Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar. Sie sollten stattdessen [**findresourcew**](/windows/win32/api/winbase/nf-winbase-findresourcea) verwenden.\]

Bestimmt den Speicherort einer Ressource mit dem angegebenen Typ und Namen im angegebenen Modul.

> [!Note]  
> **Findresourcewrapw** ist ein Wrapper für die **findresourcew** -Funktion. Weitere Hinweise zur Verwendung finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .

 

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

*HMODULE* \[ in\]
</dt> <dd>

Typ: **HMODULE**

Ein Handle für das Modul, dessen ausführbare Datei die Ressource enthält. Der Wert **null** gibt das Modul Handle an, das der Bilddatei zugeordnet ist, die vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.

</dd> <dt>

*lpname* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Der Name der Ressource. Weitere Informationen finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lptype* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die den Ressourcentyp angibt. Weitere Informationen finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **hrsrc**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für den Informationsblock der angegebenen Ressource. Um ein Handle für die Ressource zu erhalten, übergeben Sie dieses Handle an die [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) -Funktion.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**. Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine bestimmte Lokalisierung angeben müssen, verwenden Sie die Funktion [**findresourceex**](/windows/win32/api/winbase/nf-winbase-findresourceexa) anstelle von **findresourcewrapw**.

**Findresourcewrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen zu verwenden. Die bevorzugte Methode ist die Verwendung von [**findresourcew**](/windows/win32/api/winbase/nf-winbase-findresourcea) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Findresourcewrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 66 verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Findresourcewrapw** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
