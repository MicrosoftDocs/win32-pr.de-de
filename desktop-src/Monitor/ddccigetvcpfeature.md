---
title: DDCCIGetVCPFeature-Funktion
description: Ruft den aktuellen Wert, den höchstwert und den Codetyp eines VCP-Codes (Virtual Systemsteuerung) für einen Monitor ab.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- DDCCIGetVCPFeature-Funktion Monitorkonfiguration
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15549d69bb446d7a7e6d5c44517bade3e9158d1a6d5f9b9ae839d6b1b547717a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640998"
---
# <a name="ddccigetvcpfeature-function"></a>DDCCIGetVCPFeature-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Überwachungskonfigurations-API verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Ruft den aktuellen Wert, den höchstwert und den Codetyp eines VCP-Codes (Virtual Systemsteuerung) für einen Monitor ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
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

Der abzufragende VCP-Code.

</dd> <dt>

*pvct* \[ out, optional\]
</dt> <dd>

Empfängt den VCP-Codetyp als Member der [**MC \_ VCP \_ CODE \_ TYPE-Enumeration.**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type)

</dd> <dt>

*pdwCurrentValue* \[ out\]
</dt> <dd>

Empfängt den aktuellen Wert des VCP-Codes.

</dd> <dt>

*pdwMaximumValue* \[ out, optional\]
</dt> <dd>

Empfängt den maximalen Wert des VCP-Codes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) aufrufen, anstatt diese Funktion aufzurufen.

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

 

