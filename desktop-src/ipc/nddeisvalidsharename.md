---
description: Bestimmt, ob ein Freigabe Name die richtige Syntax verwendet.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Nddeisvalidsharename-Funktion (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346268"
---
# <a name="nddeisvalidsharename-function"></a>Nddeisvalidsharename-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Bestimmt, ob ein Freigabe Name die richtige Syntax verwendet.

## <a name="syntax"></a>Syntax


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShareName* \[ in\]
</dt> <dd>

Der Freigabe Name, der überprüft werden soll. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Freigabe Name eine gültige Syntax aufweist, ist der Rückgabewert ungleich 0 (null).

Wenn der Freigabe Name nicht über eine gültige Syntax verfügt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird auch von [**ndabshareadd**](nddeshareadd.md) aufgerufen, wenn Sie die DDE-Freigabe erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Nddeisvalidsharenamew** (Unicode) und **nddeisvalidsharenamea** (ANSI)<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Ndabshareadd**](nddeshareadd.md)
</dt> </dl>

 

 




