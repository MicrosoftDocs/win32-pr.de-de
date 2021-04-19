---
description: Ruft das Zertifikat aus den Anmelde Informationen des Benutzers ab.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Getcertifipeefromkred-Funktion (lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345881"
---
# <a name="getcertificatefromcred-function"></a>Getcertifipeefromkred-Funktion

Ruft das Zertifikat aus den Anmelde Informationen des Benutzers ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProviderHandle* \[ in\]
</dt> <dd>

Handle des Identitäts Anbieters.

</dd> <dt>

*Clienttoken* \[ in\]
</dt> <dd>

Das Token des Aufrufers, der das Zertifikat abruft.

</dd> <dt>

*Supplied-* \[ ID in\]
</dt> <dd>

Ein Zeiger auf eine durch [**secpkg \_ angegebene \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) Anmelde Informationsstruktur, die die Anmelde Informationen einer Online-ID enthält, deren Zertifikat angefordert wird. Der Identitäts Anbieter muss die Eingabedaten So validieren, als ob Sie aus einer nicht vertrauenswürdigen Quelle stammen.

</dd> <dt>

*Suppliedkredsize* \[ in\]
</dt> <dd>

Die Größe des *suppliedup-* Puffers in Bytes.

</dd> <dt>

*Certcontext* \[ vorgenommen\]
</dt> <dd>

Wenn die Funktion erfolgreich ausgeführt wird, ist dieser Parameter ein Zeiger auf den zurückgegebenen ccert- \_ Kontext Zeiger. Wenn Sie die Verwendung des Zertifikat Kontexts abgeschlossen haben, geben Sie ihn durch Aufrufen der [**certfreecertifipriecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion frei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion Status \_ Erfolg zurück.

Wenn die Funktion fehlschlägt, gibt die Funktion möglicherweise einen der folgenden NTSTATUS-Fehlercodes zurück.



| Rückgabewert                                                                                            | BESCHREIBUNG                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>Status \_ \_ wird nicht unterstützt</dt> </dl>       | Der Identitäts Anbieter erkennt den Anmelde Informationstyp der angegebenen Anmelde Informationen nicht. Der nächste Identitäts Anbieter wird von LSA ausprobiert.<br/>                                           |
| <dl> <dt>Fehler bei der Status \_ Anmeldung \_</dt> </dl>       | Die Anmelde Informationen sind falsch.<br/>                                                                                                                                                |
| <dl> <dt>\_ungültiger \_ Parameter.</dt> </dl>   | Ein Parameter ist nicht gültig. Die Anmelde Informationen haben möglicherweise ein falsches Format und nicht die definierte [**secpkg- \_ \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) Anmelde Informationsstruktur.<br/> |
| <dl> <dt>Status \_ Netzwerk \_ nicht erreichbar</dt> </dl> | Der Identitäts Anbieter kann keine Verbindung mit der Cloud hergestellt werden, um das Zertifikat zu erhalten.<br/>                                                                                                   |
| <dl> <dt>Status \_ Kennwort \_ abgelaufen</dt> </dl>    | Das Konto Kennwort ist abgelaufen.<br/>                                                                                                                                           |
| <dl> <dt>Status \_ Konto \_ gesperrt \_</dt> </dl> | Das Konto wurde gesperrt. <br/>                                                                                                                                           |
| <dl> <dt>Andere</dt> </dl>                       | Andere Anbieterspezifische Fehlercodes. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Bevor Sie das Zertifikat aus der Cloud abrufen, sollte der Identitäts Anbieter überprüfen, ob für diesen Benutzer ein gültiges Zertifikat im Zertifikat Speicher des Benutzers vorhanden ist. Wenn ein gültiges Zertifikat vorhanden ist, sollte der Anbieter dieses Zertifikat zurückgeben, um unnötigen Netzwerkverkehr zu vermeiden.

Der Identitäts Anbieter kann das Zertifikat auch lokal zwischenspeichern, solange es vor dem aktuellen Benutzer geschützt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

