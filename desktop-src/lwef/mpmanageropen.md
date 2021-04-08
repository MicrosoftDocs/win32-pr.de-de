---
title: Mpmanageropen-Funktion (mpclient. h)
description: Stellt eine Verbindung mit dem Malware Schutz-Manager auf dem lokalen Computer her.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Mpmanageropen-Funktion Legacy Funktionen der Windows-Umgebung
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
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743184"
---
# <a name="mpmanageropen-function"></a>Mpmanageropen-Funktion

Stellt eine Verbindung mit dem Malware Schutz-Manager auf dem lokalen Computer her.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwReserved* \[ in\]
</dt> <dd>

Typ: **DWORD**

Für die zukünftige Verwendung reserviert. Muss auf 0 festgelegt werden.

</dd> <dt>

*phmphandle* \[ vorgenommen\]
</dt> <dd>

Typ: **pmphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**. Dieser Funktions Aufrufvorgang ist garantiert auch dann erfolgreich, wenn kein antischadsoftwaredienst ausgeführt wird.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code. Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

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

[**Mplenker schließen**](mphandleclose.md)
</dt> </dl>

 

 





