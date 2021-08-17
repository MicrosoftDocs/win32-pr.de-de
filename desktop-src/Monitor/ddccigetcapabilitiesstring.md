---
title: DDCCIGetCapabilitiesString-Funktion
description: Ruft eine Zeichenfolge ab, die die Funktionen eines Monitors beschreibt.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- DDCCIGetCapabilitiesString-Funktion Monitorkonfiguration
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
ms.openlocfilehash: 2f21cf89ef459e2585dda9f05e4f16d032949d423c627225380481d71c59400d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806128"
---
# <a name="ddccigetcapabilitiesstring-function"></a>DDCCIGetCapabilitiesString-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Api für die Monitorkonfiguration verwendet, um auf die Funktionalität im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

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

*hMonitor* \[ In\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*pszString* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Funktionenzeichenfolge empfängt. Rufen Sie [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)auf, um die Länge der Funktionenzeichenfolge zu erhalten.

</dd> <dt>

*dwLength* \[ In\]
</dt> <dd>

Die Größe des *pszString-Puffers* in Zeichen, einschließlich des beendenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS zurückgegeben.** Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**CapabilitiesRequestAndCapabilitiesReply aufrufen,**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) anstatt diese Funktion auf aufruft.

Dieser Funktion ist keine Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Gdi32.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Überwachen von Konfigurationsfunktionen](monitor-configuration-functions.md)
</dt> </dl>

 

