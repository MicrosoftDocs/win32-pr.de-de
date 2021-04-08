---
description: Verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Unlockwithnumericalpassword-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862275"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Unlockwithnumericalpassword-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **unlockwithnumericalpassword** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.

Der Verschlüsselungsschlüssel des Volumes muss mit einer oder mehreren Schlüssel Schutzvorrichtungen des Typs "numerisches Kennwort" gesichert werden (mithilfe der [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode), um das Volume mit dieser Methode entsperren zu können.

> [!Note]  
> Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numericalpassword* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das numerische Kennwort angibt.

Das numerische Kennwort muss 48 Ziffern enthalten. Diese Ziffern können in 8 Gruppen mit 6 Ziffern aufgeteilt werden, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt. Jede Gruppe von 6 Ziffern muss von 11 teilbar sein und muss kleiner als 65536 sein. Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 bezeichnet wird, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.

Die Gruppen von Ziffern können optional durch ein Leerzeichen oder einen Bindestrich getrennt werden. "Xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" kann daher auch gültige numerische Kenn Wörter enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 zurück.



| Rückgabecode/-wert                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | Die Methode war erfolgreich.<br/>                                                                                                                                                                                          |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                   |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | Das Volume weist keine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" auf.<br/> Der *numericalpassword* -Parameter hat ein gültiges Format, aber Sie können kein numerisches Kennwort verwenden, um das Volume zu entsperren.<br/>           |
| <dl> <dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt> </dl>    | Der *numericalpassword* -Parameter kann das Volume nicht entsperren.<br/> Mindestens eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" ist vorhanden, aber der angegebene *numericalpassword* -Parameter kann das Volume nicht entsperren.<br/> |
| <dl> <dt>**F \_ E \_ Ungültiges Kenn \_ Wort \_ Format**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | Der *numericalpassword* -Parameter weist kein gültiges Format auf.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
