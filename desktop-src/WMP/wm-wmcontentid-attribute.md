---
title: WM/WMContentID-Attribut
description: Das WM/WMContentID-Attribut ist eine GUID, die den Inhalt des Elements identifiziert.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- WM/WMContentID-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f31a42a650d382597e2495d80541d667e229dde09a8181605d83cef65e39945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053758"
---
# <a name="wmwmcontentid-attribute"></a>WM/WMContentID-Attribut

Das **WM/WMContentID-Attribut** ist eine GUID, die den Inhalt des Elements identifiziert.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**WMContentID** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMContentID.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





