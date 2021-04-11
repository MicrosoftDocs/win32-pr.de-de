---
title: Dsrestoreprepare-Funktion (ntdsbcli. h)
description: Stellt eine Verbindung mit dem angegebenen Verzeichnisserver her und bereitet ihn für den Wiederherstellungs Vorgang vor.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Dsrestoreprepare-Funktion Active Directory
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
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103499"
---
# <a name="dsrestoreprepare-function"></a>Dsrestoreprepare-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsrestoreprepare** -Funktion stellt eine Verbindung mit dem angegebenen Verzeichnisserver her und bereitet Sie für den Wiederherstellungs Vorgang vor.

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

*szservername* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers enthält, der wieder hergestellt werden soll. Vorangehende umgekehrte Schrägstriche sind optional. Der Server muss derselbe Computer sein, von dem diese Funktion aufgerufen wird. Der Servername darf keine Unterstriche ( \_ ) enthalten. Ein Beispiel für einen Servernamen ist " \\ \\ Server1".

</dd> <dt>

*rtflag* \[ in\]
</dt> <dd>

Gibt den Typ der durchzuführenden Wiederherstellung an. Dies kann NULL oder einer der folgenden Werte sein.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**\_wiederherungstyp- \_ Erstellungen**


</dt> <dd>

Standard. Die wiederhergestellte Version ist durch die standardmäßige ababstimmungs Logik abgestimmt, sodass die wiederhergestellte DIT mit anderen Enterprise Server-Computern synchronisiert werden kann.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**\_wiederherungstyp \_ authoratativ**


</dt> <dd>

Nicht unterstützt.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**Restore \_ Type \_ Online**


</dt> <dd>

Nicht unterstützt. Die Wiederherstellung wird ausgeführt, wenn NTDS Online ist.

</dd> </dl> </dd> <dt>

*pvexpiriytoken* \[ in\]
</dt> <dd>

Zeiger auf das Ablauf Token, das der wiederhergestellten Sicherung zugeordnet ist. Dieses Token wurde von der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen, als das Verzeichnis gesichert wurde.

Wenn dieser Parameter **null** ist, kann das in *phbC* zurückgegebene Handle nur zum Abrufen der Wiederherstellungs Verzeichnisse mit der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion verwendet werden. Das Handle kann nicht für andere Wiederherstellungs Funktionen verwendet werden.

</dd> <dt>

*cbexpirydekensize* \[ in\]
</dt> <dd>

Enthält die Größe des Ablauf Tokens in *pvexpiriytoken* in Bytes.

</dd> <dt>

*phbC* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **HBC** -Wert, der das Handle für die Wiederherstellung empfängt. Dieses Handle wird verwendet, wenn andere Verzeichnisdienst-Wiederherstellungs Funktionen aufgerufen werden, wie z. b. [**dsbackupopenfile**](dsbackupopenfile.md) und [**dsrestoreend**](dsrestoreend.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird ein **HRESULT** -Standard Code zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die **dsrestoreprepare** -Funktion erfordert, dass der Aufrufer Mitglied der Gruppe "Administratoren" auf dem Server ist.

**Dsrestoreprepare** kann mit oder ohne bereitgestelltes Token verwendet werden. Wenn das Token bereitgestellt wird, wird es auf den Ablauf geprüft, und alle Vorgänge sind für den zurückgegebenen Kontext zulässig. Wenn das Token nicht bereitgestellt wird, ist der zurückgegebene Kontext eingeschränkt und darf nur für die [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion verwendet werden. Sie kann nicht für die [**dsrestoreregiester**](dsrestoreregister.md) -Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dsrestorepreparew** (Unicode) und **dsrestorepreparea** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wiederherstellen eines Active Directory Servers](restoring-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> <dt>

[**Dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**Dsrestoreregiester**](dsrestoreregister.md)
</dt> <dt>

[**Dsrestoreregistercomplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**Dsrestoreend**](dsrestoreend.md)
</dt> </dl>

 

