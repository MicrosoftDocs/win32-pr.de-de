---
description: Gibt die verschlüsselte Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042046"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>MF SampleExtension \_ Encryption \_ cryptbyteblock-Attribut

Gibt die verschlüsselte Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Die Anzahl der eindeutigen (nicht verschlüsselten) Bytes im Teilprobe-Zuordnungs Block wird im [ \_ \_ skipbyteblock-Attribut der MF SampleExtension-Verschlüsselung](mfsampleextension-encryption-skipbyteblock.md) angegeben. Wenn keines dieser Attribute vorhanden ist oder den Wert 0 hat, bedeutet dies, dass die Beispiel Daten nicht verschlüsselt sind. Beide Werte müssen einen Wert ungleich 0 (null), positive Werte aufweisen, oder beide müssen den Wert 0 (null) aufweisen.

In Fällen, in denen die Quelle MP4-basiert ist, wird der Wert basierend auf den Werten des standardmäßigen \_ crypt- \_ \_ Byteblocks innerhalb des Felds "Verschlüsselung nachverfolgen" ("tenc") im MP4-Header festgelegt. Weitere Informationen finden Sie unter [MF SampleExtension \_ Encryption \_ Protection Schema](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



 

 




