---
title: DDCCISaveCurrentSettings-Funktion
description: Speichert die aktuellen Monitoreinstellungen im nicht unwillingsfreien Speicher der Anzeige.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- DDCCISaveCurrentSettings-Funktion Monitorkonfiguration
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
ms.openlocfilehash: d1307747fca18cd1cd86d13c5718240bff260d0882a6865bd817d44632093e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013458"
---
# <a name="ddccisavecurrentsettings-function"></a>DDCCISaveCurrentSettings-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Api für die Monitorkonfiguration verwendet, um auf die Funktionalität im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Speichert die aktuellen Monitoreinstellungen im nicht unwillingsfreien Speicher der Anzeige.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hmonitor* 
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS zurückgegeben.** Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**SaveCurrentSettings aufrufen,**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) anstatt diese Funktion auf aufruft.

Dieser Funktion ist keine Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Gdi32.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Überwachen von Konfigurationsfunktionen](monitor-configuration-functions.md)
</dt> </dl>

 

