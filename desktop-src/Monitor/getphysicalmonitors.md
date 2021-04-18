---
title: Getphysicalmonitors-Funktion
description: Ruft die physischen Monitore ab, die einem Anzeigegerät zugeordnet sind.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Getphysicalmonitors-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338334"
---
# <a name="getphysicalmonitors-function"></a>Getphysicalmonitors-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Ruft die physischen Monitore ab, die einem Anzeigegerät zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrindevicename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/desktop/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.

</dd> <dt>

*dwphysicalmonitorarraysize* \[ in\]
</dt> <dd>

Die Anzahl der Elemente im *pdwnumphysicalmonitorlenker* -Array. Um die erforderliche Größe des Arrays abzurufen, nennen Sie [**getnumofphysicalmonitors**](getnumberofphysicalmonitors.md).

</dd> <dt>

*pdwnumphysicalmonitorlenker-Array* \[ vorgenommen\]
</dt> <dd>

Empfängt die Anzahl der Elemente, die die Funktion in das *phphysicalmonitorarray* -Array kopiert.

</dd> <dt>

*phphysicalmonitorarray* \[ vorgenommen\]
</dt> <dd>

Ein Array, das Handles für die physischen Monitore empfängt. Jedes Handle muss durch Aufrufen von [**destroyphysicalmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)freigegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufzurufen:

-   [**Getphysicalmonitorsfromhmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Überwachen von Konfigurationsfunktionen](monitor-configuration-functions.md)
</dt> </dl>

 

