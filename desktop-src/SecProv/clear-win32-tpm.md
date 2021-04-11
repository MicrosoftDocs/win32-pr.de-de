---
description: Setzt das TPM auf seine Werkseinstellungen zurück.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Clear-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217426"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Clear-Methode der Win32- \_ TPM-Klasse

Die **Clear** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse setzt das TPM auf den Standardzustand der Factory zurück. Ein TPM-Besitzer kann diese Methode verwenden, um den TPM-Besitz abzubrechen und kryptografiematerialien ungültig zu machen, die vom vorherigen Besitzer erstellt wurden. Diese Methode hält BitLocker an, wenn durch den Aufruf von eine BitLocker-Wiederherstellung erforderlich ist. BitLocker wird automatisch fortgesetzt, sobald TPM bereitgestellt wurde.

> [!Caution]  
> Durch das Löschen des TPM verlieren Sie alle TPM-Schlüssel, die von Anwendungen erstellt und verwendet werden. Wenn diese Schlüssel zum Verschlüsseln von Daten verwendet wurden, stellen Sie sicher, dass Sie vor dem Löschen des TPM eine andere Möglichkeit haben, auf die Daten zuzugreifen.

 

## <a name="syntax"></a>Syntax


```mof
uint32 Clear(
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

Durch das Ausführen dieser Methode kann ein TPM-Computer für die Wiederverwendung vorbereitet werden.

Um das TPM zu löschen, aber nicht mehr über die TPM-Besitzer Autorisierung verfügen, benötigen Sie physischen Zugriff auf den Computer. Die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode enthält Funktionen, die das Löschen des TPM ohne TPM-Besitzer Autorisierung erleichtern.

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

 

 
