---
description: Gibt die Größe des klar (nicht verschlüsselten) Byteblocks für die beispielbasierte Musterverschlüsselung an.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: MFSampleExtension_Encryption_SkipByteBlock -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c674a7f7762f97a1978bd827795733d01b1dea3053898c5ecd30308373449b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603130"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>MFSampleExtension \_ Encryption \_ SkipByteBlock-Attribut

Gibt die Größe des klar (nicht verschlüsselten) Byteblocks für die beispielbasierte Musterverschlüsselung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Die Anzahl der verschlüsselten Bytes im Zuordnungsblock des Untersampels wird im [ \_ \_ CryptByteBlock-Attribut der MFSampleExtension Encryption angegeben.](mfsampleextension-encryption-cryptbyteblock.md) Wenn eines dieser Attribute nicht vorhanden ist oder den Wert 0 hat, bedeutet dies, dass die Beispieldaten nicht verschlüsselt sind. Beide Werte müssen nicht 0 (null) oder positive Werte sein, oder beide müssen den Wert 0 (null) haben.

In Fällen, in denen die Quelle MP4-basiert ist, wird der Wert basierend auf den Werten des standardmäßigen Skip-Byteblocks innerhalb des Track Encryption-Felds \_ \_ \_ ("tenc") im MP4-Header festgelegt. Weitere Informationen finden Sie unter [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




