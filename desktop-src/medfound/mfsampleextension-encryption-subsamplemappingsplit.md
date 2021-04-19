---
description: Legt die unter Stichproben Zuordnung für das Beispiel fest, das die unverschlüsselten und verschlüsselten Bytes in den Beispiel Daten angibt.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356582"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>MF SampleExtension \_ Encryption \_ subsamplemappingsplit-Attribut

Legt die unter Stichproben Zuordnung für das Beispiel fest, das die unverschlüsselten und verschlüsselten Bytes in den Beispiel Daten angibt.

## <a name="data-type"></a>Datentyp

**BLOB**

## <a name="remarks"></a>Bemerkungen

Das **BLOB** muss ein Array von Byte Bereichen als DWords enthalten, wobei jede zweier DWords eine Menge macht. Das erste DWORD in jeder Gruppe ist die Anzahl der eindeutigen bytes, und das zweite DWORD des Satzes ist die Anzahl verschlüsselter Bytes. Beachten Sie, dass es sich bei einem Paar von 0s nicht um einen gültigen Satz handelt (jeder Wert kann 0 sein, aber nicht beides). Das Array von Byte Bereichen gibt an, welche Bereiche entschlüsselt werden sollen, einschließlich der Möglichkeit, dass die gesamte Stichprobe nicht entschlüsselt werden soll. Es wird empfohlen, dass dies nicht für klare Beispiele festgelegt wird, obwohl es möglich ist, dasselbe Ergebnis zu erzielen, indem es die entsprechenden Werte festlegt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie mfsampleextension \_ Encryption \_ subsamplemappingsplit festgelegt wird.


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MF SampleExtension- \_ Inhalts \_ Schlüssel-ID](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




