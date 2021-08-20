---
description: Gibt ein geschütztes Ausgabeobjekt frei.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: DestroyOPMProtectedOutput-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 5a30f4f4666b2da2e9b1fc38c90f51da9264f4656f82ac11f7abd55b498419e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742369"
---
# <a name="destroyopmprotectedoutput-function"></a>DestroyOPMProtectedOutput-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Gibt ein geschütztes Ausgabeobjekt frei.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*opoOPMProtectedOutput* \[ In\]
</dt> <dd>

Ein Handle für das geschützte Ausgabeobjekt. Dieses Handle wird durch Aufrufen von [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)abgerufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

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

 

 
