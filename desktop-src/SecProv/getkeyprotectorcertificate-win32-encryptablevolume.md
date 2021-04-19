---
description: Ruft den öffentlichen Schlüssel und den Zertifikat Fingerabdruck für die Schutzvorrichtung eines öffentlichen Schlüssels ab.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Getkeyprotectorcertificate-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364132"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Getkeyprotectorcertificate-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getkeyprotectorcertificate** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) und den [*Zertifikat*](../secgloss/c-gly.md) Fingerabdruck für die Schutzvorrichtung eines öffentlichen Schlüssels ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> <dt>

*PublicKey* \[ vorgenommen\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Bytearray, das den öffentlichen Schlüssel angibt.

</dd> <dt>

*Certthumbprint* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Zertifikat Fingerabdruck angibt.

</dd> <dt>

*Certtype* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der Schlüssel Schutzvorrichtung angibt. Diese Ganzzahl wird zur Unterscheidung zwischen Data Recovery Agent (DRA) und Benutzer Zertifikaten verwendet.



| Wert                                                                        | Bedeutung                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | Das Zertifikat ist ein DRA-.<br/>     |
| <dl> <dt>2</dt> </dl> | Das Zertifikat ist keine DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                                       | BESCHREIBUNG                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Die Methode war erfolgreich.<br/>                                                                           |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | Die angegebene Schlüssel Schutzvorrichtung ist keine Schlüssel Schutzvorrichtung. Sie müssen eine andere Schlüssel Schutzvorrichtung eingeben.<br/>            |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Dieses Laufwerk ist BitLocker-Laufwerkverschlüsselung gesperrt. Dieses Volume muss in der Systemsteuerung entsperrt werden. <br/> |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                    |
| <dl> <dt>**F \_ E \_ - \_ richtlinienbenutzerzertifikat \_ \_ erforderlich**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Gruppenrichtlinie erfordert die Verwendung eines Benutzer Zertifikats, z. b. eine Smartcard.<br/>                           |



 

## <a name="remarks"></a>Bemerkungen

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

 

 
