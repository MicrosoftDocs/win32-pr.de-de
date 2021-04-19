---
title: Ddccigetcapabilitiesstringlength-Funktion
description: Ruft die Länge einer Funktions Zeichenfolge für einen Monitor ab.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Ddccigetcapabilitiesstringlength-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339547"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a>Ddccigetcapabilitiesstringlength-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Ruft die Länge einer Funktions Zeichenfolge für einen Monitor ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hmonitor* \[ in\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*pdwLength* \[ vorgenommen\]
</dt> <dd>

Empfängt die Länge der Funktions Zeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten [**getcapabilitiesstringlength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) aufrufen, anstatt diese Funktion aufzurufen.

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

 

