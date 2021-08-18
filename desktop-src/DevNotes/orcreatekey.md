---
description: Erstellt den angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur. Wenn der Schlüssel bereits vorhanden ist, öffnet die Funktion ihn.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: ORCreateKey-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7ea5a365a9c5bdcb478ce47443a713ed5bc091666b54de880dc478708e4c36c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749690"
---
# <a name="orcreatekey-function"></a>ORCreateKey-Funktion

Erstellt den angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur. Wenn der Schlüssel bereits vorhanden ist, öffnet die Funktion ihn.

## <a name="syntax"></a>Syntax


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*lpSubKey* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen eines Unterschlüssels enthält, den diese Funktion öffnet oder erstellt. Der *lpSubKey-Parameter* muss einen Unterschlüssel des Schlüssels angeben, der durch den *Handle-Parameter* identifiziert wird. es kann bis zu 32 Ebenen tief in der Registrierungsstruktur sein. Weitere Informationen zu Schlüsselnamen finden Sie unter [Struktur der Registrierung.](../sysinfo/structure-of-the-registry.md)

Dieser Parameter darf nicht **NULL** sein.

Bei Schlüsselnamen wird die Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

*lpClass* \[ in, optional\]
</dt> <dd>

Die Klasse (Objekttyp) dieses Schlüssels. Dieser Parameter kann ignoriert werden. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*dwOptions* \[ in, optional\]
</dt> <dd>

Dieser Parameter kann 0 oder einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**REG \_ OPTION \_ CREATE \_ LINK**</dt> <dt>0x00000002L</dt> </dl>    | Der Schlüssel ist eine symbolische Verknüpfung. Der Zielpfad wird dem L"SymbolicLinkValue"-Wert des Schlüssels zugewiesen. Der Zielpfad muss ein absoluter Registrierungspfad sein. Wenn diese Option festgelegt ist, muss auch **REG \_ OPTION NON \_ \_ VOLATILE** festgelegt werden. <br/> Wenn der *lpSubKey-Parameter* einen vorhandenen Schlüssel angibt, muss er mit **REG OPTION CREATE \_ \_ \_ LINK** erstellt worden sein.<br/> Symbolische Registrierungslinks sollten nur verwendet werden, wenn dies für die Anwendungskompatibilität unbedingt erforderlich ist. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**REG \_ OPTION \_ NON \_ VOLATILE**</dt> <dt>0x00000000L</dt> </dl> | Der Schlüssel ist nicht flüchtig. Dies ist die Standardeinstellung. Die Informationen werden in einer Datei gespeichert und beim Neustart des Systems beibehalten. Die [**ORSaveHive-Funktion**](orsavehive.md) speichert Schlüssel, die nicht flüchtig sind.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [SECURITY \_ DESCRIPTOR-Struktur,](/windows/win32/api/winnt/ns-winnt-security_descriptor) die einen Sicherheitsdeskriptor für den neuen Schlüssel enthält. Wenn *pSecurityDescriptor* **NULL** ist, ruft der Schlüssel einen Standardsicherheitsdeskriptor ab. Die ACLs in einer Standardsicherheitsbeschreibung für einen Schlüssel werden vom direkten übergeordneten Schlüssel geerbt.

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den geöffneten oder erstellten Schlüssel empfängt. Verwenden Sie die [**ORCloseKey-Funktion,**](orclosekey.md) um den Schlüssel zu schließen, nachdem Sie das Handle verwendet haben.

</dd> <dt>

*pdwDisposition* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen der folgenden Dispositionswerte empfängt.



| Wert                                                                                                                                                                                                                                                          | Bedeutung                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**REG \_ CREATED \_ NEW \_ KEY**</dt> <dt>0x00000001L</dt> </dl>             | Der Schlüssel war nicht vorhanden und wurde erstellt.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**REG \_ GEÖFFNETER \_ VORHANDENER \_ SCHLÜSSEL**</dt> <dt>0x00000002L</dt> </dl> | Der Schlüssel war vorhanden und wurde einfach geöffnet, ohne geändert zu werden.<br/> |



 

Wenn *pdwDisposition* **NULL** ist, werden keine Dispositionsinformationen zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

Wenn der *dwOptions-Parameter* mit **REG OPTION CREATE \_ \_ \_ LINK** festgelegt ist, reg **OPTION NON \_ \_ \_ VOLATILE** jedoch eindeutig ist, oder wenn das zurückzugebende Handle ein Handle für den Stammschlüssel der Struktur wäre, gibt die Funktion ERROR \_ INVALID PARAMETER \_ zurück.

## <a name="remarks"></a>Hinweise

Der Schlüssel, den die **ORCreateKey-Funktion** erstellt, hat keine Werte. Eine Anwendung kann die [**ORSetValue-Funktion**](orsetvalue.md) verwenden, um Schlüsselwerte festzulegen.

Die **ORCreateKey-Funktion** kann nicht zum Erstellen des Stammschlüssels in einer Offlineregistrierungsstruktur verwendet werden. Verwenden Sie die [**ORCreateHive-Funktion,**](orcreatehive.md) um den Stammschlüssel zu erstellen und ein Handle für den Schlüssel abzurufen.

Die Offlineregistrierung unterstützt das Speichern einzelner Schlüssel nicht. Verwenden Sie die [**ORSaveHive-Funktion,**](orsavehive.md) um einen Schlüssel und seine Unterschlüssel in einer Struktur zu speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[\_SICHERHEITSBESCHREIBUNG](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
