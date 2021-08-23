---
description: Ermöglicht dem TPM-Besitzer das Deaktivieren oder Anhalten des TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Disable-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a2bd76795cceaf299843b0b47f6f798d4471c67241f7c3fa206db52060bde745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668040"
---
# <a name="disable-method-of-the-win32_tpm-class"></a>Disable-Methode der Win32 \_ Tpm-Klasse

Mit der **Disable-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) kann der TPM-Besitzer das TPM deaktivieren oder anhalten. Diese Methode hält BitLocker an, wenn der Aufruf der BitLocker-Wiederherstellung erforderlich sein könnte. BitLocker wird automatisch fortgesetzt, sobald TPM bereitgestellt wurde.

## <a name="syntax"></a>Syntax


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OwnerAuth* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den TPM-Besitzer identifiziert. Diese Zeichenfolge muss eine Base64-codierte Zeichenfolge sein, die genau 20 Bytes binärer Daten enthält. Verwenden Sie die [**ConvertToOwnerAuth-Methode,**](converttoownerauth-win32-tpm.md) um eine Passphrase in dieses erwartete Format zu übersetzen. Der *OwnerAuth-Parameter* wird aus der Registrierung gelesen, wenn kein Parameter angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                         | Beschreibung                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Die Methode war erfolgreich.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | Der angegebene Besitzerautorisierungswert kann die Anforderung nicht ausführen.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E: \_ \_ SPERRE \_ WIRD AUSGEFÜHRT 2150107139**</dt> <dt>(0x80280803)</dt> </dl> | Das TPM schützt vor Wörterbuchangriffen und befindet sich in einem Time out-Zeitraum. Weitere Informationen finden Sie in der [**ResetAuthLockOut-Methode.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**SetPhysicalPresenceRequest-Methode,**](setphysicalpresencerequest-win32-tpm.md) um das TPM zu deaktivieren, ohne den TPM-Besitzerautorisierungswert zu verwenden.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
