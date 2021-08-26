---
title: WM/Year-Attribut
description: Das WM/Year-Attribut ist das Jahr, in dem der Inhalt veröffentlicht wurde.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- WM/Year-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0b76fbf54a53a7ae09728fe34d75fff5c232de9ecfa13a77edaa97cd37e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900190"
---
# <a name="wmyear-attribute"></a>WM/Year-Attribut

Das **WM/Year-Attribut** ist das Jahr, in dem der Inhalt veröffentlicht wurde.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird nur in der digitalen Mediendatei gespeichert.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

Dieses Attribut sollte nicht als Teil einer Abfragebedingung verwendet werden. Sie wird von einem anderen Attribut abgeleitet und kann in einer Medienauflistung nicht direkt abgefragt werden.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMYear.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie Windows Media Player 10 oder höher unterstützt dieses Attribut nicht.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





