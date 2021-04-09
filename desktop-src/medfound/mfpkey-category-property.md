---
description: Enthält die Kategorie-GUID für eine Media Foundation Transformation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: MFPKEY_CATEGORY-Eigenschaft (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865576"
---
# <a name="mfpkey_category-property"></a>Eigenschaft "mfpkey \_ Category"

Enthält die Kategorie-GUID für eine Media Foundation Transformation (MFT).



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**GUID** (**CLSID** \* )

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist eine GUID, die die MFT-Kategorie bezeichnet. Eine Liste der Kategorien finden Sie unter [**MFT \_ Category**](mft-category.md).

Diese Eigenschaft ist optional und dient nur zu Informationszwecken. Eine MFT kann diese Eigenschaft verwenden, um die Kategorie zu melden, in der Sie registriert ist. Um diese Eigenschaft zu erhalten, Fragen Sie die MFT für die **IPropertyStore** -Schnittstelle ab.

Um eine MFT-Kategorie aufzulisten, müssen Sie die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion aufzurufen. Es gibt keine direkte Verknüpfung zwischen der **MF** -Funktion und dieser Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 




