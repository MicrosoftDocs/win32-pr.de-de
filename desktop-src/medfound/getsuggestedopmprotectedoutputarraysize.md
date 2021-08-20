---
description: Ruft die Größe des Arrays ab, das vor dem Aufruf von CreateOPMProtectedOutputs zugeordnet werden soll.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: GetSuggestedOPMProtectedOutputArraySize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: c84738fe37661d2a593432b571c6022b0369e28ee3b2a3cb028b8eb84276a21a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879377"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a>GetSuggestedOPMProtectedOutputArraySize-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf funktionen im Anzeigetreiber zuzugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Ruft die Größe des Arrays ab, das vor dem Aufruf von [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)zugeordnet werden soll.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrDeviceName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**UNICODE \_ STRING-Struktur,**](/windows/win32/api/subauth/ns-subauth-unicode_string) die den Namen des Anzeigegeräts enthält, wie von der [**GetMonitorInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) zurückgegeben.

</dd> <dt>

*pdwSuggestedOPMProtectedOutputArraySize* \[ out\]
</dt> <dd>

Empfängt die Größe, die für das Array zugeordnet werden soll, als Anzahl von Arrayelementen.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Funktionen](opm-functions.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 
