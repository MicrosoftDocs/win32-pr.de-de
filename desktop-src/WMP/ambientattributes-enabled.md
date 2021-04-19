---
title: Ambientattribute. aktiviert
description: Mit dem aktivierten Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement aktiviert oder deaktiviert ist.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Ambientattribute. aktivierte Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369945"
---
# <a name="ambientattributesenabled"></a>Ambientattribute. aktiviert

Mit dem **aktivierten** Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement aktiviert oder deaktiviert ist.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG               |
|-------|---------------------------|
| true  | Standard. Steuerelement aktiviert. |
| false | Steuerelement deaktiviert.         |



 

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement aktiviert ist, kann es über einen Tabstopp verfügen, und alle Ambient-Ereignisse werden empfangen. Wenn diese Option deaktiviert ist, verfügt das Steuerelement nicht über eine Tabstopp Taste und empfängt keine Umgebungs Maus-oder Tastatur Ereignisse, die darauf ausgelöst werden. (Es werden jedoch weiterhin alle anderen Ambient-Ereignisse empfangen, die darauf ausgelöst werden.)

Dieses Attribut wird für das **subview** -Element nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





