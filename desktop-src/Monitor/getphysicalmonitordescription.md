---
title: Getphysicalmonitordescription-Funktion
description: Ruft eine Beschreibung eines physischen Monitors ab.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Getphysicalmonitordescription-Funktions Monitor Konfiguration
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
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103599"
---
# <a name="getphysicalmonitordescription-function"></a>Getphysicalmonitordescription-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

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

*Hmonitor* \[ in\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*dwphysicalmonitordescriptionsizone chars* \[ in\]
</dt> <dd>

Die Anzahl der Zeichen im *szphysicalmonitordescription* -Array.

</dd> <dt>

*szphysicalmonitordescription* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array, das die Beschreibung empfängt. Die Anzahl der Elemente im Array sollte mindestens die Größe des **physischen \_ Monitors \_ \_** aufweisen.

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

 

