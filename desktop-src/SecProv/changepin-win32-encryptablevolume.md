---
description: Ändert die PIN, die einem verschlüsselten Volume zugeordnet ist.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Changepin-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525694"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Changepin-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **changepin** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " ändert die PIN, die einem verschlüsselten Volume zugeordnet ist. Wenn die Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" aktiviert ist, kann eine PIN zusätzlich zu den Zahlen Buchstaben, Symbole und Leerzeichen enthalten.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der eindeutige Zeichen folgen Bezeichner, mit dem eine verschlüsselte volumeschlüsselschutzvorrichtung verwaltet wird

</dd> <dt>

*Newpin* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine vom Benutzer angegebene persönliche Identifikations Zeichenfolge. Diese Zeichenfolge muss aus einer Sequenz von 4 bis 20 Ziffern bestehen, oder, wenn die Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" aktiviert ist, 4 bis 20 Buchstaben, Symbole, Leerzeichen oder Ziffern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**F \_ E \_ Bootable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Auf diesem Computer wurde eine Start fähige CD/DVD gefunden. Entfernen Sie die CD/DVD, und starten Sie den Computer neu.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**F \_ E \_ ungültige \_ Pin \_**</dt> -Zeichen <dt>2150695066 (0x8031009a)</dt> </dl>          | Der *newpin* -Parameter enthält ungültige Zeichen. Wenn der Gruppenrichtlinie "Erweiterte Pins für den Start zulassen" deaktiviert ist, werden nur Ziffern unterstützt.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt> </dl>     | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel". Verwenden Sie entweder die [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode oder die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode, um eine Schlüssel Schutzvorrichtung des entsprechenden Typs zu erstellen.<br/> |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**F \_ E \_ Richtlinie \_ ungültige \_ Pin- \_ Länge**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | Der angegebene *newpin* -Parameter ist entweder länger als 20 Zeichen, kürzer als 4 Zeichen oder kürzer als die durch Gruppenrichtlinie angegebene Mindestlänge.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>        | Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**TSB \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Auf diesem Computer wurde keine kompatible Trusted Platform Module (TPM) gefunden.<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Bemerkungen

Die **changepin** -Methode erstellt eine neue TPM-und PIN-Schutzvorrichtung basierend auf den vorhandenen Schutz Informationen und der neu bereitgestellten PIN. Die neue Schutzvorrichtung weist dieselbe GUID auf. Die **changepin** -Methode kann auch aufgerufen werden, um die PIN einer beliebigen Schlüssel Schutzvorrichtung zu ändern, die eine PIN verwendet, z. b. TPM und PIN oder TPM mit PIN und USB.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
