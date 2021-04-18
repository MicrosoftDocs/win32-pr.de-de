---
description: Setzt den Timeout Zeitraum oder einen anderen Mechanismus, den TPM-Hersteller implementiert, zum Schutz vor Wörterbuchangriffen auf TPM-Autorisierungs Werten zurück.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Resetauthlockout-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345680"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Resetauthlockout-Methode der Win32 \_ TPM-Klasse

Die **resetauthlockout** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse setzt den Timeout Zeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementieren, um gegen Wörterbuchangriffe auf TPM-Autorisierungs Werte zu schützen. Bei einem Wörterbuch Angriff versucht ein Angreifer, einen korrekten TPM-Autorisierungs Wert zu erraten, indem er alle möglichen Werte vollständig versucht.

Verwenden Sie diese Methode, wenn das TPM gesperrt ist, weil zu viele falsche Versuche bei der Eingabe der Besitzer Autorisierung oder anderer Autorisierungs Werte aufgetreten sind. Wenn das TPM gesperrt ist, geben einige oder alle Befehle, die für das TPM ausgegeben werden, einen Fehler zurück, TPM \_ E verteidigt die Sperre, die \_ ausgeführt wird \_ \_ (0x80280803).

> [!Note]  
> Diese Methode kann nur einmal verwendet werden, wenn das TPM gesperrt ist. Wenn die für diese Methode angegebene Besitzer Autorisierung falsch ist, wird das TPM für den gesamten Timeout Zeitraum gesperrt, und zusätzliche Versuche beim Zurücksetzen der Sperre sind nicht erfolgreich.

 

## <a name="syntax"></a>Syntax


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Besitzer *des Besitzers* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den TPM-Besitzer angibt.

Diese Zeichenfolge muss eine Base64-codierte NULL-terminierte Zeichenfolge sein, die genau 20 Bytes Binärdaten enthält. Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen. Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden. In der folgenden Tabelle sind einige der gemeinsamen Rückgabewerte aufgeführt.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | Der angegebene Besitzer Autorisierungs Wert ist falsch. Weitere Versuche, die Sperre zurückzusetzen, führen zu diesem Fehler. Warten Sie, bis der Timeout Zeitraum oder ein anderer Hersteller spezifischer Mechanismus abgelaufen ist, bevor Sie die gesperrten TPM-Befehle wiederholen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft den TPM \_ resetlockvalue-Befehl auf dem TPM auf. Das genaue Verhalten dieser Methode variiert je nach TPM-Hersteller. Die Dokumentation des Computers oder des TPM-Herstellers bietet möglicherweise zusätzliche Informationen zur Implementierung des antidictionary-Angriffs Mechanismus.

Im Allgemeinen können Hersteller von Wörterbuchangriffen erkennen, indem Sie fehlgeschlagene Authentifizierungen verfolgen. Wenn die Anzahl oder Häufigkeit von Fehlern hoch genug ist, sperrt das TPM weitere Befehle für eine bestimmte Zeit. Im Allgemeinen ist der anfängliche Timeout Zeitraum kurz, damit ein berechtigter Benutzer die Möglichkeit hat, die Situation zu beheben. Wenn der Fehler weiterhin auftritt, kann sich die Dauer der nachfolgenden Timeout Zeiten schnell erhöhen.

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

 

 
