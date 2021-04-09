---
title: Ddccisavecurrentsettings-Funktion
description: Speichert die aktuellen Monitoreinstellungen im nicht flüchtigen Speicher der Anzeige.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Konfiguration der ddccisavecurrentsettings-Funktion
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949679"
---
# <a name="ddccisavecurrentsettings-function"></a>Ddccisavecurrentsettings-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Speichert die aktuellen Monitoreinstellungen im nicht flüchtigen Speicher der Anzeige.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmonitor* 
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten [**savecurrentsettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) aufrufen, anstatt diese Funktion aufzurufen.

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

 

