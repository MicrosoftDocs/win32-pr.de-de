---
description: Ermöglicht dem TPM-Besitzer das Aktivieren oder Fortsetzen des TPM.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Enable-Methode der Win32_Tpm Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: ce3103b3845a56a8de8ba4245a2803ef7bcb7624a4781dc658c48ff277354796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004548"
---
# <a name="enable-method-of-the-win32_tpm-class"></a>Enable-Methode der Win32 \_ Tpm-Klasse

Mit **der Enable-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) kann der TPM-Besitzer das TPM aktivieren oder fortsetzen.

Um diese Methode ausführen zu können, muss das TPM bereits über einen Besitzer verfügen. Verwenden Sie die [**SetPhysicalPresenceRequest-Methode,**](setphysicalpresencerequest-win32-tpm.md) um ein TPM zu aktivieren, das noch nicht über einen Besitzer verfügt.

## <a name="syntax"></a>Syntax


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OwnerAuth* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den TPM-Besitzer identifiziert. Diese Zeichenfolge muss eine Base64-codierte Zeichenfolge sein, die genau 20 Bytes binärer Daten enthält. Verwenden Sie [**die ConvertToOwnerAuth-Methode,**](converttoownerauth-win32-tpm.md) um eine Passphrase in dieses erwartete Format zu übersetzen. Der *OwnerAuth-Parameter* wird aus der Registrierung gelesen, wenn kein Parameter angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler und -Fehler, die für TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                         | Beschreibung                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Die Methode war erfolgreich.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | Der bereitgestellte Autorisierungswert des Besitzers kann die Anforderung nicht ausführen.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ DEFEND LOCK RUNNING \_ \_ 2150107139**</dt> <dt>(0x80280803)</dt> </dl> | Das TPM wird gegen Wörterbuchangriffe geschützt und befindet sich in einem Time out-Zeitraum. Weitere Informationen finden Sie unter [**ResetAuthLockOut-Methode.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
