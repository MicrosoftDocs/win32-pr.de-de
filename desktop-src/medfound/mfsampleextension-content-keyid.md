---
description: Legt die Schlüssel-ID für das Beispiel fest.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: MFSampleExtension_Content_KeyID-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368232"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>MF Sample Extension- \_ Content \_ keyid-Attribut

Legt die Schlüssel-ID für das Beispiel fest.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie die Schlüssel-ID für das Beispiel festgelegt wird.


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
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

[MF SampleExtension \_ Encryption \_ subsamplemappingsplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




