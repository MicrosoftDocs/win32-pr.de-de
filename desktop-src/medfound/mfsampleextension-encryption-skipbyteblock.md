---
description: Gibt die eindeutige (nicht verschlüsselte) Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: MFSampleExtension_Encryption_SkipByteBlock-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863971"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>\_Skipbyteblock-Attribut für MF SampleExtension-Verschlüsselung \_

Gibt die eindeutige (nicht verschlüsselte) Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Die Anzahl verschlüsselter Bytes im Teilprobe-Zuordnungs Block wird im Attribut " [ \_ \_ cryptbyteblock" der MF SampleExtension-Verschlüsselung](mfsampleextension-encryption-cryptbyteblock.md) angegeben. Wenn keines dieser Attribute vorhanden ist oder den Wert 0 hat, bedeutet dies, dass die Beispiel Daten nicht verschlüsselt sind. Beide Werte müssen einen Wert ungleich 0 (null), positive Werte aufweisen, oder beide müssen den Wert 0 (null) aufweisen.

In Fällen, in denen die Quelle MP4-basiert ist, wird der Wert basierend auf den Werten des \_ standardskip- \_ \_ Byteblocks innerhalb des Felds "Verschlüsselung nachverfolgen" ("tenc") im MP4-Header festgelegt. Weitere Informationen finden Sie unter [MF SampleExtension \_ Encryption \_ Protection Schema](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



 

 




