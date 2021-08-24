---
title: GetPhysicalMonitors-Funktion
description: Ruft die physischen Monitore ab, die einem Anzeigegerät zugeordnet sind.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- GetPhysicalMonitors-Funktion Monitorkonfiguration
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
ms.openlocfilehash: f94cef0352aae75f95b1ff7ee9e65937f82c7b598a19cdce768028173dc97331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146153"
---
# <a name="getphysicalmonitors-function"></a>GetPhysicalMonitors-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Überwachungskonfigurations-API verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

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

*pstrDeviceName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**UNICODE \_ STRING-Struktur,**](/windows/desktop/api/subauth/ns-subauth-unicode_string) die den Namen des Anzeigegeräts enthält, wie von der [**GetMonitorInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) zurückgegeben.

</dd> <dt>

*dwPhysicalMonitorArraySize* \[ In\]
</dt> <dd>

Die Anzahl der Elemente im *array pdwNumPhysicalMonitorHandlesInArray.* Rufen [**Sie GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)auf, um die erforderliche Größe des Arrays abzurufen.

</dd> <dt>

*pdwNumPhysicalMonitorHandlesInArray* \[ out\]
</dt> <dd>

Empfängt die Anzahl der Elemente, die die Funktion in das *array phPhysicalMonitorArray* kopiert.

</dd> <dt>

*phPhysicalMonitorArray* \[ out\]
</dt> <dd>

Ein Array, das Handles für die physischen Monitore empfängt. Jedes Handle muss durch Aufrufen von [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)freigegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufrufen:

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

Dieser Funktion ist keine Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Überwachen von Konfigurationsfunktionen](monitor-configuration-functions.md)
</dt> </dl>

 

