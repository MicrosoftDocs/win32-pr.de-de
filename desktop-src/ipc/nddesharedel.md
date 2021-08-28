---
description: Löscht eine DDE-Freigabe aus dem DDE-Freigabedatenbank-Manager (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: NDdeShareDel-Funktion (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0efd5bb41712e8bee2ee7a5e789d1b006a490c932b48386de27f56a8b1150f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611100"
---
# <a name="nddesharedel-function"></a>NDdeShareDel-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Löscht eine DDE-Freigabe aus dem DDE-Freigabedatenbank-Manager (DSDM).

## <a name="syntax"></a>Syntax


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*lpszShareName* \[ In\]
</dt> <dd>

Der Name der Freigabe, die aus dem DSDM gelöscht werden soll. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*wReserved* \[ In\]
</dt> <dd>

Reserviert. Dieser Parameter muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Hinweise

Um eine DDE-Freigabe aus dem DSDM zu löschen, müssen Sie über die entsprechenden Berechtigungen verfügen. Der Ersteller der Freigabe verfügt über Löschberechtigungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeShareDelW** (Unicode) und **NDdeShareDelA** (ANSI)<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht dynamische Daten Exchange Netzwerksicherheit](network-dynamic-data-exchange.md)
</dt> <dt>

[DDE-Netzwerkfunktionen](network-dde-functions.md)
</dt> </dl>

 

 




