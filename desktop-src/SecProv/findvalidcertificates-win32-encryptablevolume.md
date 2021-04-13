---
description: Listet alle Zertifikate auf dem System auf, die mit den angegebenen Kriterien übereinstimmen, und gibt eine Liste von Fingerabdrücken zurück.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Findvalidzertifikate-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347258"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Findvalidzertifikats-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **findvalidzertifikate** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " listet alle Zertifikate auf dem System auf, die den angegebenen Kriterien entsprechen, und gibt eine Liste von Fingerabdrücken zurück. Die zurückgegebene Liste enthält nur Zertifikate mit einem gültigen [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID). Die OID ist möglicherweise der Standardwert oder kann im Gruppenrichtlinie angegeben werden.

## <a name="syntax"></a>Syntax


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Certifi-ethumschlag-Druck* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein Array von Zeichen folgen, das die Liste gültiger Zertifikate enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                           | BESCHREIBUNG                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Die Methode war erfolgreich.<br/>                |
| <dl> <dt>**F \_ E \_ ungültige \_ BitLocker- \_ OID**</dt> <dt>2150695022 (0x8031006e)</dt> </dl> | Die verfügbare BitLocker-OID ist ungültig.<br/> |



 

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

 

 
