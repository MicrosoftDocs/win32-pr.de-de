---
description: Installiert einen Besitzer für das TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: TakeOwnership-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050428"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>TakeOwnership-Methode der Win32- \_ TPM-Klasse

Mit der **TakeOwnership** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse wird ein Besitzer für das TPM installiert. Der Besitzer des TPM kann die TPM-Funktionen in vollem Umfang nutzen. Nachdem ein Besitzer festgelegt wurde, kann kein anderer Benutzer oder keine Software den Besitz des TPM beanspruchen.

Die Methoden [**is-aktiviert**](isenabled-win32-tpm.md), [**isaktiviert**](isactivated-win32-tpm.md)und [**isownershipallowed**](isownershipallowed-win32-tpm.md) müssen alle zutreffen, bevor die **TakeOwnership** -Methode erfolgreich ausgeführt werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Besitzer *des Besitzers* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den TPM-Besitzer angibt. Diese Zeichenfolge muss eine Base64-codierte NULL-terminierte Zeichenfolge sein, die genau 20 Bytes Binärdaten enthält. Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen. Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.



| Rückgabecode/-wert                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Die Methode war erfolgreich.<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Der Parameter " *besitzauth* " ist ungültig.<br/>                                                                                                                                                                 |
| <dl> <dt>**TPM \_ E- \_ Besitzer \_ Satz**</dt> <dt>2150105108 (0x80280014)</dt> </dl>            | Ein Besitzer ist bereits auf dem TPM vorhanden.<br/>                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ keine \_ Bestätigung**</dt> <dt>2150105123 (0x80280023)</dt> </dl>       | Es wurde kein Endorsement Key auf dem TPM gefunden.<br/> Informationen zum Erstellen eines Endorsement Key-Paars auf dem TPM finden Sie unter der Methode " [**kreateendorsegmentkeypair**](createendorsementkeypair-win32-tpm.md) ".<br/>             |
| <dl> <dt>**TPM \_ E \_ Installation \_ deaktiviert**</dt> <dt>2150105099 (0x8028000b)</dt> </dl>     | Ein Besitzer kann nicht auf diesem TPM installiert werden.<br/> Informationen dazu, wie Sie die Installation eines Geräte Besitzers zulassen, finden Sie unter [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md).<br/> |
| <dl> <dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt> </dl> | Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum. Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.<br/>                               |



 

## <a name="remarks"></a>Bemerkungen

Die Methoden [](isenabled-win32-tpm.md) [**isaktivierte, isaktivierte**](isactivated-win32-tpm.md)und [**isownershipallowed**](isownershipallowed-win32-tpm.md) müssen alle wahr sein, damit der **Take Ownership** -Vorgang erfolgreich ausgeführt werden kann.

Sie sollten die [**convertdebesitzauth**](converttoownerauth-win32-tpm.md) -Methode verwenden, um eine Passphrase in den Eingabe Wert zu ändern, der für den Parameter " *besitzauth* " verwendet wird.

Die **TakeOwnership** -Methode sichert den Besitzer Autorisierungs Wert, um Active Directory, wenn die entsprechenden Gruppenrichtlinie Einstellungen konfiguriert wurden.

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

 

 
