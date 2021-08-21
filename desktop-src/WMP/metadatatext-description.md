---
title: MetadataText.description
description: Die description-Eigenschaft ruft eine Beschreibung des Metadatentexts ab.
ms.assetid: df8c9c0f-7ae9-42e8-bca6-9dc42e899212
keywords:
- MetadataText.description Windows Media Player
topic_type:
- apiref
api_name:
- MetadataText.description
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae13af8adba3bd44c4db67beebabd65639957db8e29f085038b489907b8935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836940"
---
# <a name="metadatatextdescription"></a>MetadataText.description

Die **description-Eigenschaft** ruft eine Beschreibung des Metadatentexts ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **getItemInfoByType**( *name*, *language*, *index*). **Beschreibung**

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

[**MetadataText-Objekt**](metadatatext-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





