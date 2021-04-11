---
description: Ermöglicht dem TPM-Besitzer, das TPM zu aktivieren oder fortzusetzen.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Enable-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216191"
---
# <a name="enable-method-of-the-win32_tpm-class"></a>Enable-Methode der Win32- \_ TPM-Klasse

Mit der **enable** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse kann der TPM-Besitzer das TPM aktivieren oder fortsetzen.

Zum Ausführen dieser Methode muss das TPM bereits über einen Besitzer verfügen. Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um ein TPM zu aktivieren, das nicht bereits über einen Besitzer verfügt.

## <a name="syntax"></a>Syntax


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Besitzer *des Besitzers* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den TPM-Besitzer angibt. Bei dieser Zeichenfolge muss es sich um eine Base64-codierte Zeichenfolge handeln, die genau 20 Byte Binärdaten enthält. Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen. Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Die Methode war erfolgreich.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | Der angegebene Besitzer Autorisierungs Wert kann die Anforderung nicht ausführen.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt> </dl> | Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum. Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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
</dt> <dt>

[**Setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
