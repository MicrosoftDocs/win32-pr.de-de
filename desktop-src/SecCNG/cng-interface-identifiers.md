---
description: Die folgenden Bezeichner werden verwendet, um eine kryptografische CNG-Schnittstelle zu identifizieren.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: CNG-Schnittstellenbezeichner (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ebadf561df916eedde1175a39911da55628b113022378cee9e74b61d021792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908271"
---
# <a name="cng-interface-identifiers"></a>CNG-Schnittstellenbezeichner

Die folgenden Bezeichner werden verwendet, um eine kryptografische CNG-Schnittstelle zu identifizieren. In CNG identifiziert eine Schnittstelle den Typ des kryptografischen Verhaltens, das ein Anbieter unterstützt. Ein Anbieter kann beispielsweise ein Zufallszahlengenerator oder ein Hashanbieter sein.



| Konstante/Wert                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ \_VERSCHLÜSSELUNGSSCHNITTSTELLEN-0X00000001**</dt> <dt></dt> </dl>                                               | Die symmetrische Verschlüsselungsschnittstelle.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ HASH \_ INTERFACE**</dt> <dt>0x00000002</dt> </dl>                                                     | Die Hashschnittstelle.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ ASYMMETRIC \_ ENCRYPTION \_ INTERFACE**</dt> <dt>0X00000003</dt> </dl> | Die asymmetrische Verschlüsselungsschnittstelle.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ SCHNITTSTELLENSCHNITTSTELLE \_ \_ FÜR**</dt> <dt>GEHEIME 0X00000004</dt> </dl>                | Die Schnittstelle für die Geheimvereinbarung.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ \_SIGNATURSCHNITTSTELLEN-0X00000005**</dt> <dt></dt> </dl>                                      | Die Signaturschnittstelle.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ \_RNG-0X00000006**</dt> <dt></dt> </dl>                                                        | Die Zufallszahlengenerator-Schnittstelle.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ KEY \_ STORAGE \_ INTERFACE**</dt> <dt>0X00010001</dt> </dl>                               | Die Schlüsselspeicherschnittstelle.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ \_SCHANNEL-0X00010002**</dt> <dt></dt> </dl>                                         | Die Schannel-Signaturschnittstelle.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ SCHANNEL \_ SIGNATURE \_ INTERFACE**</dt> <dt>0X00010003</dt> </dl>          | Die Schannel-Cipher Suite-Schnittstelle.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP und Windows 2000:** Dieser Wert wird nicht unterstützt.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h; </dt> <dt>Ncrypt.h</dt> </dl> |



 

 




