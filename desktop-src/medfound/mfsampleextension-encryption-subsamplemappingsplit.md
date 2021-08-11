---
description: Legt die Unterbeispielzuordnung für das Beispiel fest, die die eindeutigen und verschlüsselten Bytes in den Beispieldaten angibt.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f10f845b337ab92774f36b46940fe9d5203ca3a672f573e33fbcea26e96e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240793"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>MFSampleExtension \_ Encryption \_ SubSampleMappingSplit-Attribut

Legt die Unterbeispielzuordnung für das Beispiel fest, die die eindeutigen und verschlüsselten Bytes in den Beispieldaten angibt.

## <a name="data-type"></a>Datentyp

**Blob**

## <a name="remarks"></a>Hinweise

Das **BLOB** sollte ein Array von Bytebereichen als DWORDs enthalten, wobei alle zwei DWORDs einen Satz machen. Das erste DWORD in jeder Menge ist die Anzahl der eindeutigen Bytes, und das zweite DWORD der Menge ist die Anzahl der verschlüsselten Bytes. Beachten Sie, dass ein 0s-Paar kein gültiger Satz ist (beide Werte können 0 sein, aber nicht beide). Das Array von Bytebereichen gibt an, welche Bereiche entschlüsselt werden sollen, einschließlich der Möglichkeit, dass das gesamte Beispiel nicht entschlüsselt werden soll. Es wird empfohlen, dies nicht für eindeutige Stichproben festzulegen, obwohl es möglich ist, das gleiche Ergebnis zu erzielen, indem Sie es mit den entsprechenden Werten festlegen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie MFSampleExtension \_ Encryption \_ SubSampleMappingSplit festgelegt wird.


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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**DIESSAMPLE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ Content \_ KeyID](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




