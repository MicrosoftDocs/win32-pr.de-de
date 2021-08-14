---
title: DsRestoreEnd-Funktion (Ntdsbcli.h)
description: Wird aufgerufen, um einen Wiederherstellungsvorgang zu beenden.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- DsRestoreEnd-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fbea2559517f6cc541d89817ab32c9d1992da4907f399b94830b41b1b0c1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191816"
---
# <a name="dsrestoreend-function"></a>DsRestoreEnd-Funktion

\[Diese Funktion ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsRestoreEnd-Funktion** wird aufgerufen, um einen Wiederherstellungsvorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbc* \[ In\]
</dt> <dd>

Enthält das Mit der [**DsRestorePrepare-Funktion erhaltene Wiederherstellungskontexthand**](dsrestoreprepare.md) handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK zurück,** wenn die Funktion erfolgreich ist, andernfalls ein Win32- oder RPC-Fehlercode. In der folgenden Liste sind mögliche Fehlercodes aufgeführt.

<dl> <dt>

**FEHLER \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd>

*hbc* ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **DsRestoreEnd-Funktion** schließt ausstehende Bindungshandles und führt nach einem Wiederherstellungsversuch einen Bereinigungsvorgang aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Nicht unterstützt<br/>                                                               |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[Wiederherstellen eines Active Directory-Servers](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

