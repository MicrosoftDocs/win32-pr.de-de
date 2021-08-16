---
title: MpManagerOpen-Funktion (MpClient.h)
description: Stellt eine Verbindung mit dem Malwareschutz-Manager auf dem lokalen Computer her.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- MpManagerOpen-Funktion – Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324d013c46777ac48af32e6c91f557b7feda3a03fbdf0c21a7c79e8cf5e3d9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883365"
---
# <a name="mpmanageropen-function"></a>MpManagerOpen-Funktion

Stellt eine Verbindung mit dem Malwareschutz-Manager auf dem lokalen Computer her.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwReserved* \[ In\]
</dt> <dd>

Typ: **DWORD**

Für die zukünftige Verwendung reserviert. Muss auf 0 festgelegt werden.

</dd> <dt>

*phMpHandle* \[ out\]
</dt> <dd>

Typ: **PMPHANDLE**

Behandeln Sie die Schnittstelle des Schadsoftwareschutz-Managers. Dieses Handle muss mit der [**MpHandleClose-Funktion**](mphandleclose.md) geschlossen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **S \_ OK.** Dieser Funktionsaufruf ist auch dann erfolgreich, wenn kein AntiMalware-Dienst ausgeführt wird.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





