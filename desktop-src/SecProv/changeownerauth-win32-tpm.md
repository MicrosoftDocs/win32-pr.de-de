---
description: Ändert den TPM-Besitzer Autorisierungs Wert.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Changebesitzauth-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128760"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Changebesitzauth-Methode der Win32- \_ TPM-Klasse

Mit der **changebesitzauth** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse wird der TPM-Besitzer Autorisierungs Wert geändert.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Oldownerauth* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den aktuellen TPM-Besitzer Autorisierungs Wert des Geräts benennt. Verwenden Sie die [**convertdebesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um ein Kennwort in diesen Autorisierungs Wert zu übersetzen. Der *oldownerauth* -Parameter wurde nicht angegeben, oder es wird eine leere Zeichenfolge bereitgestellt. diese Methode ruft den Wert aus der Registrierung ab, falls vorhanden.

</dd> <dt>

" *Netwownerauth* \[ " in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den neuen TPM-Besitzer Autorisierungs Wert benennt. Verwenden Sie die [**convertdebesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um ein Kennwort in diesen Autorisierungs Wert zu übersetzen. Der Parameter " *netwownerauth* " darf nicht leer oder **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                              | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | Der aktuelle TPM-Besitzer Autorisierungs Wert ist falsch.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt> </dl>      | Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum. Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**F \_ E \_ AD- \_ Schema \_ nicht \_ installiert**</dt> <dt>2150694922 (0x8031000a)</dt> </dl> | Wiederherstellungs Informationen können nicht im Netzwerk gespeichert werden. Der Computer wurde so konfiguriert, dass Wiederherstellungs Informationen in Active Directory Domain Services gespeichert werden. Anweisungen zum Einrichten von Active Directory finden Sie [unter BitLocker-Laufwerkverschlüsselung Configuration Guide: Sichern von BitLocker-und TPM-Wiederherstellungs Informationen in Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).<br/> |
| <dl> <dt>**Verbindungs**</dt> Fehler <dt>2147943755 (0x8007054b)</dt> </dl>                  | Wiederherstellungs Informationen können nicht im Netzwerk gespeichert werden. Der Computer wurde so konfiguriert, dass Wiederherstellungs Informationen in Active Directory Domain Services gespeichert werden. Eine Netzwerkverbindung ist erforderlich, um den Vorgang fortzusetzen.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Die **changebesitzauth** -Methode sichert die neue TPM-Besitzer Autorisierung, um Active Directory Domain Services, wenn die entsprechenden Gruppenrichtlinie Einstellungen konfiguriert wurden.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
