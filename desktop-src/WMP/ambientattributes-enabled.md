---
title: AmbientAttributes.enabled
description: Das enabled-Attribut gibt einen Wert an, der angibt, ob das Steuerelement aktiviert oder deaktiviert ist, oder ruft einen Wert ab.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes.enabled-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d8e000d64ef92212cd7c6cf37c7fd79036107e1d3be0d7669d73b40c759de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055178"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes.enabled

Das **enabled-Attribut** gibt einen Wert an, der angibt, ob das Steuerelement aktiviert oder deaktiviert ist, oder ruft einen Wert ab.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG               |
|-------|---------------------------|
| true  | Standard. Steuerelement aktiviert. |
| false | Steuerelement deaktiviert.         |



 

## <a name="remarks"></a>Hinweise

Wenn das Steuerelement aktiviert ist, kann es über einen Tabstopp verfügen und alle Umgebungsereignisse empfangen. Wenn es deaktiviert ist, verfügt das Steuerelement nicht über einen Tabstopp und erhält keine Umgebungsmaus- oder Tastaturereignisse, die darauf ausgelöst werden. (Es werden jedoch weiterhin alle anderen Umgebungsereignisse empfangen, die dafür ausgelöst werden.)

Dieses Attribut wird für das **SUBVIEW-Element nicht** unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





