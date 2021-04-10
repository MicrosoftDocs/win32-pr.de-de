---
description: Sendet eine zertifizierte COPP-Status Anforderung (Output Protection Protocol) an ein geschütztes Ausgabe Objekt.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: Getcoppcompatibleopminformation-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214308"
---
# <a name="getcoppcompatibleopminformation-function"></a>Getcoppcompatibleopminformation-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Sendet eine zertifizierte COPP-Status Anforderung (Output Protection Protocol) an ein geschütztes Ausgabe Objekt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *opoopmprotectedoutput* \[ " in\]
</dt> <dd>

Ein Handle für das geschützte Ausgabe Objekt. Dieses Handle wird durch Aufrufen von [**createopmprotectedoutputs**](createopmprotectedoutputs.md)abgerufen.

</dd> <dt>

*pparameters* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **dxgkmdt \_ OPM \_ COPP- \_ kompatible \_ get \_ Info \_ Parameters** -Struktur, die Eingabedaten für die Status Anforderung enthält.

</dd> <dt>

*prequestedinformation* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine von **dxgkmdt \_ OPM \_ angeforderte \_ Informations** Struktur, die die Ergebnisse der Status Anforderung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) aufrufen, anstatt diese Funktion aufzurufen.

Das geschützte Ausgabe Objekt muss mit der COPP-Semantik erstellt werden. Siehe " [**kreateopmprotectedoutputs**](createopmprotectedoutputs.md)".

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Funktionen](opm-functions.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 
