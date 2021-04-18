---
title: Ddccigetcapabilitiesstring-Funktion
description: Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Ddccigetcapabilitiesstring-Funktions Monitor Konfiguration
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338540"
---
# <a name="ddccigetcapabilitiesstring-function"></a>Ddccigetcapabilitiesstring-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hmonitor* \[ in\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*pszstring* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Funktions Zeichenfolge empfängt. Um die Länge der Funktions Zeichenfolge abzurufen, nennen Sie [**ddccigetcapabilitiesstringlength**](ddccigetcapabilitiesstringlength.md).

</dd> <dt>

*dwLength* \[ in\]
</dt> <dd>

Die Größe des *pszstring* -Puffers in Zeichen, einschließlich des abschließenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten [**capabilitiesrequestandcapabilitiesreply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) aufrufen, anstatt diese Funktion aufzurufen.

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

 

