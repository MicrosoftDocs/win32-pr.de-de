---
title: GetPhysicalMonitorDescription-Funktion
description: Ruft eine Beschreibung eines physischen Monitors ab.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- GetPhysicalMonitorDescription-Funktion Monitorkonfiguration
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251c24db32271802b94bd2beb7a381cc9b3adb50dd97842203947ea6a6895583
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534890"
---
# <a name="getphysicalmonitordescription-function"></a>GetPhysicalMonitorDescription-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Überwachungskonfigurations-API verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Ruft eine Beschreibung eines physischen Monitors ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMonitor* \[ In\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*dwPhysicalMonitorDescriptionSizeInChars* \[ In\]
</dt> <dd>

Die Anzahl der Zeichen im *szPhysicalMonitorDescription-Array.*

</dd> <dt>

*szPhysicalMonitorDescription* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array, das die Beschreibung empfängt. Die Anzahl der Elemente im Array sollte mindestens **PHYSICAL \_ MONITOR DESCRIPTION \_ \_ SIZE** sein.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Überwachen von Konfigurationsfunktionen](monitor-configuration-functions.md)
</dt> </dl>

 

