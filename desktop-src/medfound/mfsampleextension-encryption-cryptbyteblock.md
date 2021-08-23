---
description: Gibt die verschlüsselte Byteblockgröße für die stichprobenbasierte Musterverschlüsselung an.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85da01a8b69fa22604cc10df54aa474ec117256ebee0630e490e25d9888484d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603200"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>MFSampleExtension \_ Encryption \_ CryptByteBlock-Attribut

Gibt die verschlüsselte Byteblockgröße für die stichprobenbasierte Musterverschlüsselung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Die Anzahl der eindeutigen (nicht verschlüsselten) Bytes im Subsamplezuordnungsblock wird im [MFSampleExtension \_ Encryption \_ SkipByteBlock-Attribut](mfsampleextension-encryption-skipbyteblock.md) angegeben. Wenn eines dieser Attribute nicht vorhanden ist oder den Wert 0 aufweist, bedeutet dies, dass die Beispieldaten nicht verschlüsselt sind. Beide Werte müssen ungleich 0 (null) sein, positive Werte, oder beide müssen den Wert 0 (null) aufweisen.

In Fällen, in denen die Quelle MP4-basiert ist, wird der Wert basierend auf den Werten des \_ standardmäßigen crypt-Byteblocks innerhalb des Felds für \_ die \_ Nachverfolgungsverschlüsselung ("tenc") im MP4-Header festgelegt. Weitere Informationen finden Sie unter [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




