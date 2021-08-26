---
description: Ruft das Zertifikat aus den Benutzeranmeldeinformationen ab.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: GetCertificateFromCred-Funktion (Lsaidprov.h)
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
ms.openlocfilehash: 3660fd4cfb8baa3e025789a2cde9dc04dd7e1e1678b0516a56562f1ea5be43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994481"
---
# <a name="getcertificatefromcred-function"></a>GetCertificateFromCred-Funktion

Ruft das Zertifikat aus den Benutzeranmeldeinformationen ab.

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

*ProviderHandle* \[ In\]
</dt> <dd>

Identitätsanbieterhandle.

</dd> <dt>

*ClientToken* \[ In\]
</dt> <dd>

Token des Aufrufers, der das Zertifikat abruft.

</dd> <dt>

*SuppliedCred* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SECPKG \_ SUPPLIED \_ CREDENTIAL-Struktur,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) die die Anmeldeinformationen einer Online-ID enthält, deren Zertifikat angefordert wird. Der Identitätsanbieter muss die Eingabedaten so überprüfen, als ob sie aus einer nicht vertrauenswürdigen Quelle stammen.

</dd> <dt>

*SuppliedCredSize* \[ In\]
</dt> <dd>

Die Größe des *SuppliedCred-Puffers* in Bytes.

</dd> <dt>

*CertContext* \[ out\]
</dt> <dd>

Wenn die Funktion erfolgreich ist, ist dieser Parameter ein Zeiger auf den zurückgegebenen CCERT \_ CONTEXT-Zeiger. Wenn Sie die Verwendung des Zertifikatkontexts abgeschlossen haben, geben Sie ihn frei, indem Sie die [**CertFreeCertificateContext-Funktion**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion STATUS \_ SUCCESS zurück.

Wenn die Funktion fehlschlägt, gibt die Funktion möglicherweise einen der folgenden NTSTATUS-Fehlercodes zurück.



| Rückgabewert                                                                                            | Beschreibung                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>STATUS \_ WIRD NICHT \_ UNTERSTÜTZT</dt> </dl>       | Der Identitätsanbieter erkennt den Anmeldeinformationstyp der angegebenen Anmeldeinformationen nicht. LSA versucht den nächsten Identitätsanbieter.<br/>                                           |
| <dl> <dt>FEHLER BEI DER \_ STATUSANMELDUNG \_</dt> </dl>       | Die Anmeldeinformationen sind falsch.<br/>                                                                                                                                                |
| <dl> <dt>STATUS \_ UNGÜLTIGER \_ PARAMETER</dt> </dl>   | Ein Parameter ist nicht gültig. Die Anmeldeinformationen können in einem falschen Format und nicht in der definierten [**SECPKG \_ SUPPLIED \_ CREDENTIAL-Struktur vorliegen.**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential)<br/> |
| <dl> <dt>STATUSNETZWERK \_ \_ NICHT ERREICHBAR</dt> </dl> | Der Identitätsanbieter kann sich nicht an die Cloud wenden, um das Zertifikat zu erhalten.<br/>                                                                                                   |
| <dl> <dt>\_STATUSKENNWORT \_ ABGELAUFEN</dt> </dl>    | Das Kontokennwort ist abgelaufen.<br/>                                                                                                                                           |
| <dl> <dt>STATUSKONTO \_ \_ GESPERRT \_</dt> </dl> | Das Konto wurde gesperrt. <br/>                                                                                                                                           |
| <dl> <dt>Andere</dt> </dl>                       | Andere anbieterspezifische Fehlercodes. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Vor dem Abrufen des Zertifikats aus der Cloud sollte der Identitätsanbieter überprüfen, ob im Zertifikatspeicher "MY" des Benutzers ein gültiges Zertifikat für diesen Benutzer vorhanden ist. Wenn ein gültiges Zertifikat vorhanden ist, sollte der Anbieter dieses Zertifikat zurückgeben, um unnötigen Netzwerkdatenverkehr zu vermeiden.

Der Identitätsanbieter kann das Zertifikat auch lokal zwischenspeichern, solange es vor dem aktuellen Benutzer geschützt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Lsaidprov.h</dt> </dl> |



 

