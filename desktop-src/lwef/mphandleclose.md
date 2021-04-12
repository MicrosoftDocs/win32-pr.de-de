---
title: Mplenker Close-Funktion (mpclient. h)
description: Schließt das von mpmanageropen, mpscanstart, mporial Open oder mpupdatestart zurückgegebene Handle.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Mplenker Close-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518755"
---
# <a name="mphandleclose-function"></a>Mplenker Close-Funktion

Schließt das von [**mpmanageropen**](mpmanageropen.md), [**mpscanstart**](mpscanstart.md), [**mporial Open**](mpthreatopen.md)oder [**mpupdatestart**](mpupdatestart.md)zurückgegebene Handle.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle, das geschlossen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code. Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

Der folgende spezifische Fehler kann von der-Funktion zurückgegeben werden:

| Rückgabe Code             | BESCHREIBUNG                      |
|-------------------------|----------------------------------|
| E \_ Win \_ ungültiges \_ handle | Das angegebene Handle ist ungültig. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mperrormessageformat**](mperrormessageformat.md)
</dt> <dt>

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[**Mpscanstart**](mpscanstart.md)
</dt> <dt>

[**Mpbedrohlich öffnen**](mpthreatopen.md)
</dt> </dl>

 

 





