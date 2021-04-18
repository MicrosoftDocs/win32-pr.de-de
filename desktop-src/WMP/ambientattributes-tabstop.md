---
title: Ambientattribute. Tabstopps
description: Mit dem Tabstopps-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Steuerelement in der Tabstopps-Reihenfolge befindet Sie legen die Reihenfolge der Tabstopps fest, indem Sie das-Steuerelement im gesamten Skript vor oder nach anderen Steuerelement Tags platzieren.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Ambientattribute. tabstoppwindows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365769"
---
# <a name="ambientattributestabstop"></a>Ambientattribute. Tabstopps

Mit dem Tabstopps-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Steuerelement in der **Tabstopps** -Reihenfolge befindet Sie legen die Reihenfolge der Tabstopps fest, indem Sie das-Steuerelement im gesamten Skript vor oder nach anderen Steuerelement Tags platzieren.

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Das Steuerelement befindet sich in der Tabulator Reihenfolge (das Steuerelement verfügt über eine Tabstopp Anforderung). |
| false | Das Steuerelement befindet sich nicht in der Reihenfolge der Registerkarten.                                                       |



 

## <a name="remarks"></a>Bemerkungen

Das **Tabstopps** -Attribut ist für das **Effects** -Element nicht anwendbar.

Der Standardwert für dieses Attribut ist true für alle Elemente außer **automenu** und **Text**, die den Standardwert false aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





