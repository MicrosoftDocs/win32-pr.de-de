---
title: MetadataPicture.mimeType
description: Die mimeType-Eigenschaft ruft den MIME-Standardtyp des Metadatenbilds ab.
ms.assetid: dde541e3-ddbc-437e-a3a8-64a116e122e0
keywords:
- MetadataPicture.mimeType-Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture.mimeType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9cfc6607bc121b18b7d8550576b84d251dd7f2812094a51464265e4135fa0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647700"
---
# <a name="metadatapicturemimetype"></a>MetadataPicture.mimeType

Die **mimeType-Eigenschaft** ruft den MIME-Standardtyp des Metadatenbilds ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **getItemInfoByType**( *name*, *language*, *index*). **mimeType**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge.**

## <a name="remarks"></a>Hinweise

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MetadataPicture-Objekt**](metadatapicture-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





