---
description: Konfiguriert ein geschütztes Ausgabeobjekt.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: ConfigureOPMProtectedOutput-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f62d310526d95cf4ab6d1727a3ba43eec147f320b04c0692a89d52305b7f3589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743547"
---
# <a name="configureopmprotectedoutput-function"></a>ConfigureOPMProtectedOutput-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Konfiguriert ein geschütztes Ausgabeobjekt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
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

Ein Zeiger auf eine **DXGKMDT \_ OPM \_ CONFIGURE \_ PARAMETERS-Struktur,** die den Konfigurationsbefehl enthält.

</dd> <dt>

*ulAdditionalParametersSize* \[ In\]
</dt> <dd>

Die Größe des *pbAdditionalParameters-Puffers* in Bytes.

</dd> <dt>

*pbAdditionalParameters* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der zusätzliche Informationen für den Befehl enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen sollten [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) aufrufen, anstatt diese Funktion aufzurufen.

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

 

 
