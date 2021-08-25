---
description: Setzt den Time out-Zeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementieren, um sich vor Wörterbuchangriffen auf TPM-Autorisierungswerte zu schützen.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: ResetAuthLockOut-Methode der Win32_Tpm Klasse
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
ms.openlocfilehash: 779ae7e8578019215e0bab1091512c64d68a84675d702ea7a0d8a5c37e8f081f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906300"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>ResetAuthLockOut-Methode der Win32 \_ Tpm-Klasse

Die **ResetAuthLockOut-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) setzt den Timeoutzeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementieren, um vor Wörterbuchangriffen auf TPM-Autorisierungswerte zu schützen. Bei einem Wörterbuchangriff versucht ein Angreifer, einen richtigen TPM-Autorisierungswert zu erraten, indem er alle möglichen Werte vollständig versucht.

Verwenden Sie diese Methode, wenn das TPM aufgrund zu vieler falscher Versuche, die Besitzerautorisierung oder andere Autorisierungswerte eineingaben, gesperrt ist. Wenn das TPM gesperrt ist, geben einige oder alle für das TPM ausgegebenen Befehle einen Fehler zurück: TPM \_ E DEFEND LOCK RUNNING \_ \_ \_ (0x80280803).

> [!Note]  
> Diese Methode kann nur genau einmal verwendet werden, wenn das TPM gesperrt ist. Wenn die für diese Methode bereitgestellte Besitzerautorisierung falsch ist, wird das TPM für den gesamten Time out-Zeitraum gesperrt, und zusätzliche Versuche zum Zurücksetzen der Sperre fehlschlagen.

 

## <a name="syntax"></a>Syntax


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OwnerAuth* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den TPM-Besitzer identifiziert.

Diese Zeichenfolge muss eine base64-codierte NULL-terminierte Zeichenfolge sein, die genau 20 Bytes binärer Daten enthält. Verwenden Sie [**die ConvertToOwnerAuth-Methode,**](converttoownerauth-win32-tpm.md) um eine Passphrase in dieses erwartete Format zu übersetzen. Der *OwnerAuth-Parameter* wird aus der Registrierung gelesen, wenn kein Parameter angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler und -Fehler, die für TPM-Basisdienste spezifisch sind, können zurückgegeben werden. In der folgenden Tabelle sind einige der allgemeinen Rückgabewerte aufgeführt.



| Rückgabecode/-wert                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | Der bereitgestellte Autorisierungswert des Besitzers ist falsch. Bei weiteren Versuchen, die Sperre zurücksetzungen, tritt der gleiche Fehler auf. Warten Sie, bis der Time out-Zeitraum oder ein anderer herstellerspezifischer Mechanismus abgelaufen ist, bevor Sie versuchen, gesperrte TPM-Befehle erneut auszuführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft den \_ TPM-Befehl ResetLockValue auf dem TPM auf. Das genaue Verhalten dieser Methode variiert je nach TPM-Hersteller. Die Dokumentation des Computers oder TPM-Herstellers enthält möglicherweise zusätzliche Informationen zur Implementierung des Antiwörterbuch-Angriffsmechanismus.

Im Allgemeinen können Hersteller Wörterbuchangriffe erkennen, indem sie fehlgeschlagene Authentifizierungen nachverfolgen. Wenn die Anzahl oder Häufigkeit von Fehlern hoch genug ist, sperrt das TPM weitere Befehle für einen bestimmten Zeitraum. Im Allgemeinen ist der anfängliche Time out-Zeitraum kurz, damit ein berechtigter Benutzer die Möglichkeit hat, die Situation zu korrigieren. Wenn die Fehler fortgesetzt werden, kann die Dauer jedes nachfolgenden Time out-Zeitraums schnell zunehmen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_Win32-tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
