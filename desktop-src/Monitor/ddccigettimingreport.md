---
title: DDCCIGetTimingReport-Funktion
description: Ruft die horizontalen und vertikalen Synchronisierungshäufigkeiten eines Monitors ab.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- DDCCIGetTimingReport-Funktion Monitorkonfiguration
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 930149ebc2acfa69f479c889c6fa2c33acdfb3f528a67f83ee0bfbe7ab0467a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382363"
---
# <a name="ddccigettimingreport-function"></a>DDCCIGetTimingReport-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Überwachungskonfigurations-API verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Ruft die horizontalen und vertikalen Synchronisierungshäufigkeiten eines Monitors ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMonitor* \[ In\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*pmtr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**MC \_ TIMING \_ REPORT-Struktur,**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) die die Zeitsteuerungsinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) aufrufen, anstatt diese Funktion aufzurufen.

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

 

