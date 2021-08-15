---
description: Listet alle Zertifikate im System auf, die den angegebenen Kriterien entsprechen, und gibt eine Liste von Fingerabdrucks zurück.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: FindValidCertificates-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: da642ff24fa01d27c74a30af7de6c7f91e33a712a28c47644a7044f43c40d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892438"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>FindValidCertificates-Methode der Win32 \_ EncryptableVolume-Klasse

Die **FindValidCertificates-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) listet alle Zertifikate im System auf, die den angegebenen Kriterien entsprechen, und gibt eine Liste von Fingerabdruckdaten zurück. Die zurückgegebene Liste enthält nur Zertifikate mit einem gültigen [*Objektbezeichner*](../secgloss/o-gly.md) (OID). Die OID kann die Standardeinstellung sein, oder sie kann in der Gruppenrichtlinie.

## <a name="syntax"></a>Syntax


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CertificateThumbprint* \[ out\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein Array von Zeichenfolgen, das die Liste der gültigen Zertifikate enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                           | BESCHREIBUNG                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Die Methode war erfolgreich.<br/>                |
| <dl> <dt>**FVE \_ E \_ INVALID \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl> | Die verfügbare BitLocker-OID ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
