---
description: Erstellt den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur. Wenn der Schlüssel bereits vorhanden ist, wird er von der Funktion geöffnet.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Orkreatekey-Funktion (offreg. h)
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
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369226"
---
# <a name="orcreatekey-function"></a>Orkreatekey-Funktion

Erstellt den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur. Wenn der Schlüssel bereits vorhanden ist, wird er von der Funktion geöffnet.

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

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*lpsubkey* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen eines unter Schlüssels enthält, der von dieser Funktion geöffnet oder erstellt wird. Der *lpsubkey* -Parameter muss einen Unterschlüssel des Schlüssels angeben, der durch den *handle* -Parameter identifiziert wird. Es kann bis zu 32 Ebenen tief in der Registrierungs Struktur sein. Weitere Informationen zu Schlüsselnamen finden Sie unter [Struktur der Registrierung](../sysinfo/structure-of-the-registry.md).

Dieser Parameter darf nicht **null** sein.

Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

*lpclass* \[ in, optional\]
</dt> <dd>

Die Klasse (Objekttyp) dieses Schlüssels. Dieser Parameter kann ignoriert werden. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*dwOptions* \[ in, optional\]
</dt> <dd>

Dieser Parameter kann 0 oder einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**Reg \_ Option \_ Create \_ Link**</dt> <dt>0x00000002l</dt> </dl>    | Der Schlüssel ist eine symbolische Verknüpfung. Der Zielpfad wird dem L-Wert "symboliclinkvalue" des Schlüssels zugewiesen. Der Zielpfad muss ein absoluter Registrierungs Pfad sein. Wenn diese Option festgelegt ist, muss auch die **reg \_ Option \_ nicht \_ flüchtig** festgelegt werden. <br/> Wenn der *lpsubkey* -Parameter einen vorhandenen Schlüssel angibt, muss er mit der **reg- \_ Option \_ Create \_ Link** erstellt worden sein.<br/> Symbolische Verknüpfungen für die Registrierung sollten nur verwendet werden, wenn die Anwendungs Kompatibilität absolut notwendig ist. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**Reg \_ Option \_ nicht \_ flüchtig**</dt> <dt>0x00000000L</dt> </dl> | Der Schlüssel ist nicht flüchtig. Dies ist die Standardeinstellung. Die Informationen werden in einer Datei gespeichert und beibehalten, wenn das System neu gestartet wird. Die [**orsavehive**](orsavehive.md) -Funktion speichert Schlüssel, die nicht flüchtig sind.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*psecuritydescriptor* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [Sicherheits \_ deskriptorstruktur](/windows/win32/api/winnt/ns-winnt-security_descriptor) , die eine Sicherheits Beschreibung für den neuen Schlüssel enthält. Wenn *psecuritydescriptor* den Wert **null** hat, erhält der Schlüssel eine Standard Sicherheits Beschreibung. Die ACLs in einer Standard Sicherheits Beschreibung für einen Schlüssel werden von seinem direkten übergeordneten Schlüssel geerbt.

</dd> <dt>

*phkResult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den geöffneten oder erstellten Schlüssel empfängt. Verwenden Sie die [**orclosekey**](orclosekey.md) -Funktion, um den Schlüssel zu schließen, nachdem Sie die Verwendung des Handles abgeschlossen haben.

</dd> <dt>

*pdwdisposition* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen der folgenden Dispositions Werte empfängt.



| Wert                                                                                                                                                                                                                                                          | Bedeutung                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**Reg \_ \_Neuer \_ Schlüssel**</dt> <dt>0x00000001l</dt> erstellt </dl>             | Der Schlüssel ist nicht vorhanden und wurde erstellt.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**Reg \_ Der \_ vorhandene \_ Schlüssel**</dt> <dt>0x00000002l</dt> wurde geöffnet. </dl> | Der Schlüssel war vorhanden und wurde einfach geöffnet, ohne geändert zu werden.<br/> |



 

Wenn *pdwdisposition* auf **null** festgelegt ist, werden keine Disposition-Informationen zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn der *dwOptions* -Parameter mit der **reg- \_ Option \_ Create \_ Link** festgelegt ist, aber die **reg- \_ Option \_ nicht \_ flüchtig** auf Clear festgelegt ist oder wenn das zurück zugegende Handle ein Handle für den Stamm Schlüssel der Hive ist, gibt die Funktion den \_ ungültigen Parameter Error zurück \_ .

## <a name="remarks"></a>Bemerkungen

Der Schlüssel, der von der **orkreatekey** -Funktion erstellt wird, weist keine Werte auf. Eine Anwendung kann die [**orsetvalue**](orsetvalue.md) -Funktion verwenden, um Schlüsselwerte festzulegen.

Die **orkreatekey** -Funktion kann nicht verwendet werden, um den Stamm Schlüssel in einer Offline Registrierungs Struktur zu erstellen. Verwenden Sie die [**orkreatehive**](orcreatehive.md) -Funktion, um den Stamm Schlüssel zu erstellen, und rufen Sie ein Handle für den Schlüssel ab.

Die Offline Registrierung unterstützt das Speichern einzelner Schlüssel nicht. Verwenden Sie die [**orsavehive**](orsavehive.md) -Funktion, um einen Schlüssel und dessen Unterschlüssel in einer Hive zu speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orclosekey**](orclosekey.md)
</dt> <dt>

[**Orkreatehive**](orcreatehive.md)
</dt> <dt>

[**Ordeletekey**](ordeletekey.md)
</dt> <dt>

[**Orsavehive**](orsavehive.md)
</dt> <dt>

[Sicherheits \_ Beschreibung](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
