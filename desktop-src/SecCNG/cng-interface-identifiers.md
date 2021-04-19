---
description: Die folgenden Bezeichner werden verwendet, um eine CNG-Kryptografieschnittstelle zu identifizieren.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: CNG-Schnittstellen Bezeichner (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346271"
---
# <a name="cng-interface-identifiers"></a>CNG-Schnittstellen Bezeichner

Die folgenden Bezeichner werden verwendet, um eine CNG-Kryptografieschnittstelle zu identifizieren. In CNG identifiziert eine Schnittstelle den Typ des kryptografieverhaltens, das von einem Anbieter unterstützt wird. Ein Anbieter kann z. b. ein Zufallszahlengenerator oder ein Hash Anbieter sein.



| Konstante/Wert                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**Bcrypt \_ Chiffre \_ Schnittstelle**</dt> <dt>0x00000001</dt> </dl>                                               | Die symmetrische Chiffre Schnittstelle.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**Bcrypt \_ Hash \_ Schnittstelle**</dt> <dt>0x00000002</dt> </dl>                                                     | Die Hash Schnittstelle.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**Bcrypt \_ Asymmetrische \_ Verschlüsselungs \_ Schnittstelle**</dt> <dt>0x00000003</dt> </dl> | Die asymmetrische Verschlüsselungs Schnittstelle.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**Bcrypt \_ Geheimer Vereinbarungs \_ \_ Schnittstelle**</dt> <dt>0x00000004</dt> </dl>                | Die Geheimnis Vertrags Schnittstelle.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**Bcrypt \_ Signatur \_ Schnittstelle**</dt> <dt>0x00000005 bei der</dt> </dl>                                      | Die Signatur Schnittstelle.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**Bcrypt \_ RNG- \_ Schnittstelle**</dt> <dt>0x00000006</dt> </dl>                                                        | Die Zufallszahlengenerator-Schnittstelle.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCrypt \_ Schlüssel \_ Speicher \_ Schnittstelle**</dt> <dt>0x00010001</dt> </dl>                               | Die Schlüsselspeicher Schnittstelle.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCrypt \_ SChannel- \_ Schnittstelle**</dt> <dt>0x00010002</dt> </dl>                                         | Die SChannel-Signatur Schnittstelle.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCrypt \_ SChannel- \_ Signatur \_ Schnittstelle**</dt> <dt>0x00010003</dt> </dl>          | Die SChannel Verschlüsselungs Suite-Schnittstelle.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP und Windows 2000:** Dieser Wert wird nicht unterstützt.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                |
| Header<br/>                   | <dl> <dt>Bcrypt. h; </dt> <dt>Ncrypt. h</dt> </dl> |



 

 




