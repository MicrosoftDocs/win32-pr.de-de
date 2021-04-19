---
title: Effekte. Zuweisung
description: Mit dem Attribut "attribuwall" wird ein Wert angegeben oder abgerufen, der angibt, ob alle Visualisierungen eingeschlossen werden sollen, die in der Registrierung enthalten sind.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- Effekte. Zuweisung-Windows-Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369447"
---
# <a name="effectsallowall"></a>Effekte. Zuweisung

Mit dem Attribut " **attribuwall** " wird ein Wert angegeben oder abgerufen, der angibt, ob alle Visualisierungen eingeschlossen werden sollen, die in der Registrierung enthalten sind.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                         |
|-------|---------------------------------------------------------------------|
| true  | Standard. Ermöglicht das Radfahren aller Visualisierungen auf dem System des Benutzers. |
| false | Beschränkt das Radfahren auf Visualisierungen, die in **Effekten** -Tags angezeigt werden. |



 

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut auf false festgelegt ist, können nur die Visualisierungen, die in **Effects** -Tags angezeigt werden, mithilfe von Previous/Next durchlaufen werden. Wenn der Wert auf true festgelegt ist, können alle Visualisierungen, die auf dem System des Benutzers registriert sind, durchlaufen werden. Wenn Sie auf true festgelegt ist und Sie alle Visualisierungen innerhalb von **Effects** -Tags angeben, werden die in diesen Tags angegebenen Attribute auf alle Visualisierungen im System des Benutzers angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Effects-Element**](effects-element.md)
</dt> </dl>

 

 





