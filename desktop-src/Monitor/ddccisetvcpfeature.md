---
title: DDCCISetVCPFeature-Funktion
description: Legt den Wert eines VCP-Codes (Virtual Systemsteuerung) für einen Monitor fest.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- DDCCISetVCPFeature-Funktion Monitorkonfiguration
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecbfb6172ffd61dd7882895c0db15baddf28986493b202e2fd873135cee41d76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806148"
---
# <a name="ddccisetvcpfeature-function"></a>DDCCISetVCPFeature-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Überwachungskonfigurations-API verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Legt den Wert eines VCP-Codes (Virtual Systemsteuerung) für einen Monitor fest.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMonitor* \[ In\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*dwVCPCode* \[ In\]
</dt> <dd>

Der festzulegende VCP-Code.

</dd> <dt>

*dwNewValue* \[ In\]
</dt> <dd>

Der Wert des VCP-Codes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) aufrufen, anstatt diese Funktion aufzurufen.

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

 

