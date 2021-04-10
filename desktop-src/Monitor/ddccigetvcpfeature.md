---
title: Ddccigetvcpfeature-Funktion
description: Ruft den aktuellen Wert, den maximalen Wert und den Codetyp eines virtuellen System Steuerungs Codes (VCP) für einen Monitor ab.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Monitor Konfiguration für ddccigetvcpfeature-Funktion
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
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956440"
---
# <a name="ddccigetvcpfeature-function"></a>Ddccigetvcpfeature-Funktion

> [!IMPORTANT]
> Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Ruft den aktuellen Wert, den maximalen Wert und den Codetyp eines virtuellen System Steuerungs Codes (VCP) für einen Monitor ab.

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

*Hmonitor* \[ in\]
</dt> <dd>

Ein Handle für einen physischen Monitor.

</dd> <dt>

*dwvcpcode* \[ in\]
</dt> <dd>

Der VCP-Code, der abgefragt werden soll.

</dd> <dt>

*PVCT* \[ Out, optional\]
</dt> <dd>

Empfängt den VCP-Codetyp als Member der [**MC \_ VCP- \_ \_ Codetyp**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) -Enumeration.

</dd> <dt>

*pdwcurrentvalue* \[ vorgenommen\]
</dt> <dd>

Empfängt den aktuellen Wert des VCP-Codes.

</dd> <dt>

*pdwmaximumvalue* \[ Out, optional\]
</dt> <dd>

Empfängt den maximalen Wert des VCP-Codes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten [**getvcpfeatureandvcpfeaturereply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) aufrufen, anstatt diese Funktion aufzurufen.

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

 

