---
description: Ruft den öffentlichen Schlüssel und den Zertifikatfingerabdruck für eine Schutzvorrichtung für öffentliche Schlüssel ab.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: GetKeyProtectorCertificate-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: e947cb5fadefa6703ab4515ddd8d2a9daf1e7439e514e75c64d3b1e6e885aa0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892063"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorCertificate-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectorCertificate-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) ruft den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) und den Zertifikatfingerabdruck für eine Schutzvorrichtung für öffentliche Schlüssel ab. [](../secgloss/c-gly.md)

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

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*PublicKey* \[ out\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, das den öffentlichen Schlüssel angibt.

</dd> <dt>

*CertThumbprint* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Zertifikatfingerabdruck angibt.

</dd> <dt>

*CertType* \[ out\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die den Typ der Schlüsselschutzvorrichtung angibt. Diese ganze Zahl wird verwendet, um zwischen Datenwiederherstellungs-Agent (DRA) und Benutzerzertifikaten zu unterscheiden.



| Wert                                                                        | Bedeutung                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | Das Zertifikat ist eine DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | Das Zertifikat ist keine DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                                       | BESCHREIBUNG                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Die Methode war erfolgreich.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | Die angegebene Schlüsselschutzvorrichtung ist keine Schlüsselschutzvorrichtung. Sie müssen eine andere Schlüsselschutzvorrichtung eingeben.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Dieses Laufwerk wird durch BitLocker-Laufwerkverschlüsselung gesperrt. Sie müssen dieses Volume aus Systemsteuerung entsperren. <br/> |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                    |
| <dl> <dt>**FVE \_ E \_ \_ \_ RICHTLINIENBENUTZERZERTIFIKAT \_ ERFORDERLICH**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Gruppenrichtlinie erfordert die Verwendung eines Benutzerzertifikats, z. B. einer Smartcard.<br/>                           |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, nur Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
