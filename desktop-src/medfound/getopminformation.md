---
description: Sendet eine OPM-Statusanforderung an ein geschütztes Ausgabeobjekt.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: GetOPMInformation-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bd9912289d17085bf94f3ef8316869ffb29d3a5adead4e10fc0e6d24844f4ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777300"
---
# <a name="getopminformation-function"></a>GetOPMInformation-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Sendet eine OPM-Statusanforderung an ein geschütztes Ausgabeobjekt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*opoOPMProtectedOutput* \[ In\]
</dt> <dd>

Ein Handle für das geschützte Ausgabeobjekt. Dieses Handle wird durch Aufrufen von [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)abgerufen.

</dd> <dt>

*pParameters* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **DXGKMDT \_ OPM \_ GET INFO \_ \_ PARAMETERS-Struktur,** die Eingabedaten für die Statusanforderung enthält.

</dd> <dt>

*pRequestedInformation* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **DXGKMDT \_ OPM \_ REQUESTED \_ INFORMATION-Struktur,** die die Ergebnisse der Statusanforderung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) aufrufen, anstatt diese Funktion aufzurufen.

Das geschützte Ausgabeobjekt muss mit OPM-Semantik erstellt werden. Weitere Informationen finden [**Sie unter CreateOPMProtectedOutputs.**](createopmprotectedoutputs.md)

Dieser Funktion ist keine Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[OPM-Funktionen](opm-functions.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 
