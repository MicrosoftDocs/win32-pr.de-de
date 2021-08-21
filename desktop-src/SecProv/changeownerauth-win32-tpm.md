---
description: Ändert den Wert der TPM-Besitzerautorisierung.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: ChangeOwnerAuth-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 02ca13049df20c57eeb5cc594bde1b247df0eb3829c757b64b8bd31f87e3796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004678"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>ChangeOwnerAuth-Methode der Win32 \_ Tpm-Klasse

Die **ChangeOwnerAuth-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) ändert den Tpm-Besitzerautorisierungswert.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldOwnerAuth* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den aktuellen TPM-Besitzerautorisierungswert des Geräts benennt. Verwenden Sie die [**ConvertToOwnerAuth-Methode,**](converttoownerauth-win32-tpm.md) um ein Kennwort in diesen Autorisierungswert zu übersetzen. Der *OldOwnerAuth-Parameter* wird nicht angegeben, oder es wird eine leere Zeichenfolge angegeben. Diese Methode ruft den Wert aus der Registrierung ab, sofern vorhanden.

</dd> <dt>

*NewOwnerAuth* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den neuen Wert für die TPM-Besitzerautorisierung benennt. Verwenden Sie die [**ConvertToOwnerAuth-Methode,**](converttoownerauth-win32-tpm.md) um ein Kennwort in diesen Autorisierungswert zu übersetzen. Der *NewOwnerAuth-Parameter* darf nicht leer oder **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                              | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | Der aktuelle Wert für die TPM-Besitzerautorisierung ist falsch.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E: \_ \_ SPERRE \_ WIRD AUSGEFÜHRT 2150107139**</dt> <dt>(0x80280803)</dt> </dl>      | Das TPM schützt vor Wörterbuchangriffen und befindet sich in einem Time out-Zeitraum. Weitere Informationen finden Sie in der [**ResetAuthLockOut-Methode.**](resetauthlockout-win32-tpm.md)<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ AD SCHEMA NICHT INSTALLIERT \_ \_ \_ 2150694922**</dt> <dt>(0x8031000A)</dt> </dl> | Wiederherstellungsinformationen können nicht im Netzwerk gespeichert werden. Der Computer wurde so konfiguriert, dass Wiederherstellungsinformationen in Active Directory Domain Services gespeichert werden. Anweisungen zum Einrichten von Active Directory finden Sie unter [BitLocker-Laufwerkverschlüsselung-Konfigurationshandbuch: Sichern von BitLocker- und TPM-Wiederherstellungsinformationen in Active Directory.](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10))<br/> |
| <dl> <dt>**Verbindungsfehler**</dt> <dt>2147943755 (0x8007054B)</dt> </dl>                  | Wiederherstellungsinformationen können nicht im Netzwerk gespeichert werden. Der Computer wurde so konfiguriert, dass Wiederherstellungsinformationen in Active Directory Domain Services gespeichert werden. Eine Netzwerkverbindung ist erforderlich, um fortzufahren.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Hinweise

Mit der **ChangeOwnerAuth-Methode** wird die neue TPM-Besitzerautorisierung auf Active Directory Domain Services gesichert, wenn die entsprechenden Gruppenrichtlinie Einstellungen konfiguriert wurden.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
