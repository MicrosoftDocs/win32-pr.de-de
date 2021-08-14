---
title: DsRestorePrepare-Funktion (Ntdsbcli.h)
description: Stellt eine Verbindung mit dem angegebenen Verzeichnisserver und bereitet ihn für den Wiederherstellungsvorgang vor.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- DsRestorePrepare-Funktion Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191806"
---
# <a name="dsrestoreprepare-function"></a>DsRestorePrepare-Funktion

\[Diese Funktion ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Ab Windows Vista verwenden Sie stattdessen [Volumeschattenkopie-Dienst (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

Die **DsRestorePrepare-Funktion** stellt eine Verbindung mit dem angegebenen Verzeichnisserver und bereitet sie für den Wiederherstellungsvorgang vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szServerName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des wiederherzustellenden Servers enthält. Vorangehende schräge Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keine Unterstriche \_ () enthalten. Ein Beispiel für einen Servernamen ist \\ \\ "server1".

</dd> <dt>

*rtFlag* \[ In\]
</dt> <dd>

Gibt den Typ der durchzuführenden Wiederherstellung an. Dies kann 0 (null) oder einer der folgenden Werte sein.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE \_ TYPE \_ CATCHUP**


</dt> <dd>

Standard. Die wiederhergestellte Version wird über die Standardabstimmungslogik abgestimmt, sodass die wiederhergestellte DIT mit anderen Unternehmensservercomputern synchronisiert werden kann.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE \_ TYPE \_ AUTHORATATIVE**


</dt> <dd>

Nicht unterstützt.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE \_ TYPE \_ ONLINE**


</dt> <dd>

Nicht unterstützt. Die Wiederherstellung erfolgt, wenn NTDS online ist.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ In\]
</dt> <dd>

Zeiger auf das Ablauftoken, das der wiederherzustellenden Sicherung zugeordnet ist. Dieses Token wurde von der [**DsBackupPrepare-Funktion**](dsbackupprepare.md) beim Sichern des Verzeichnisses erhalten.

Wenn dieser Parameter **NULL ist,** kann das in *phbc* zurückgegebene Handle nur zum Abrufen der Wiederherstellungsverzeichnisse mit der [**DsRestoreGetDatabaseLocations-Funktion verwendet**](dsrestoregetdatabaselocations.md) werden. Das Handle kann nicht für andere Wiederherstellungsfunktionen verwendet werden.

</dd> <dt>

*cbExpiryTokenSize* \[ In\]
</dt> <dd>

Enthält die Größe des Ablauftokens in *pvExpiryToken* in Bytes.

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Zeiger auf einen **HBC-Wert,** der das Handle für die Wiederherstellung empfängt. Dieses Handle wird beim Aufrufen anderer Wiederherstellungsfunktionen des Verzeichnisdiensts verwendet, z. B. [**DsBackupOpenFile**](dsbackupopenfile.md) und [**DsRestoreEnd.**](dsrestoreend.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt einen **HRESULT-Standardcode** zurück. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **DsRestorePrepare-Funktion** erfordert, dass der Aufrufer Mitglied der Gruppe Administratoren auf dem Server ist.

**DsRestorePrepare** kann mit oder ohne bereitgestelltes Token verwendet werden. Wenn das Token bereitgestellt wird, wird es auf Ablauf überprüft, und alle Vorgänge sind für den zurückgegebenen Kontext zulässig. Wenn das Token nicht bereitgestellt wird, ist der zurückgegebene Kontext eingeschränkt und kann nur für die [**DsRestoreGetDatabaseLocations-Funktion verwendet**](dsrestoregetdatabaselocations.md) werden. Sie darf nicht für die [**DsRestoreRegister-Funktion verwendet**](dsrestoreregister.md) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DsRestorePrepareW** (Unicode) und **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Wiederherstellen eines Active Directory-Servers](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnissicherungsfunktionen](directory-backup-functions.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> </dl>

 

