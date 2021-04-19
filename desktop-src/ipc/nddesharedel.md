---
description: Löscht eine DDE-Freigabe aus dem DDE-Freigabe Datenbank-Manager (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Nddebug-Funktion (nddecoapi. h)
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
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346675"
---
# <a name="nddesharedel-function"></a>Nddebug-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Löscht eine DDE-Freigabe aus dem DDE-Freigabe Datenbank-Manager (DSDM).

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

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*lpszsharename* \[ in\]
</dt> <dd>

Der Name der Freigabe, die aus der DSDM gelöscht werden soll. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*wReserved* \[ in\]
</dt> <dd>

Reserviert. Dieser Parameter muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.

## <a name="remarks"></a>Bemerkungen

Um eine DDE-Freigabe aus der DSDM zu löschen, müssen Sie über die entsprechenden Berechtigungen verfügen. Der Freigabe Ersteller verfügt über die Berechtigung "Löschen".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Nddeaktiviert** (Unicode) und **nddebug** (ANSI)<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> </dl>

 

 




