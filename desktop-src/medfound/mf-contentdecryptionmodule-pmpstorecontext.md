---
description: Gibt eine Kontext Zeichenfolge an, die von CDM-Implementierungen (Content entschlüsseln Module) verwendet wird, die mediaschutzpmpserver verwenden.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356603"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>Eigenschaft "MF \_ contentdecryptionmodule \_ pmpstorecontext"

Gibt eine Kontext Zeichenfolge an, die von CDM-Implementierungen (Content entschlüsseln Module) verwendet wird, die [mediaschutzpmpserver](/uwp/api/windows.media.protection.mediaprotectionpmpserver)verwenden.


## <a name="data-type"></a>Datentyp

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>Eigenschaften-GUID

**MF \_ contentdecryptionmodule \_ pmpstorecontext**

## <a name="property-value"></a>Eigenschaftswert

Eine Kontext Zeichenfolge, die von CDM-Implementierungen (Content entschlüsseln Module) verwendet wird.

## <a name="remarks"></a>Bemerkungen

Der CDM-Implementierer sollte nach diesem Wert suchen und den Wert mit dem Eigenschaftsnamen "Windows. Media. Protection. pmpstorecontext" an den [mediaschutzpmpserver-Konstruktor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) übergeben.


Apps sollten diese Eigenschaft nicht erstellen, wenn Sie [imfcontentdecryptionmoduleaccess:: createcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020-Update<br/>                                     |
| Header<br/>                   | <dl> <dt>MF contentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

- [Eigenschaften von Media Foundation](media-foundation-properties.md)
- [Mediaschutzpmpserver](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




