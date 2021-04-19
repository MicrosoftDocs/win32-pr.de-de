---
title: Ambientattribute. Passthrough
description: Durch das Passthrough-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement alle Mausereignisse an das Steuerelement darunter übergibt.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Ambientattribute. Passthrough-Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367600"
---
# <a name="ambientattributespassthrough"></a>Ambientattribute. Passthrough

Durch das **Passthrough** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement alle Mausereignisse an das Steuerelement darunter übergibt.

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                            |
|-------|--------------------------------------------------------|
| true  | Das Steuerelement übergibt Ereignisse an das Steuerelement darunter. |
| false | Standard. Das Steuerelement übergibt Ereignisse nicht durch.         |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nützlich, wenn ein Text Steuerelement z. b. auf einem Schaltflächen-Steuerelement nur zur Angabe der Bezeichnung liegt. In diesem Fall müssen Klicks auf das Text Steuerelement an das Schaltflächen-Steuerelement weitergegeben werden.

Das **Passthrough** -Attribut wird von den Elementen " **View**", " **subview**" und " **Playlist** " nicht unterstützt. Es funktioniert nicht mit dem **Video** -Element, wenn es sich um *Video* handelt. **Windows less** ist auf false festgelegt, ebenso wie das **Effects** -Element bei *Effekten*. " **Fenster** " ist auf "true" festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





