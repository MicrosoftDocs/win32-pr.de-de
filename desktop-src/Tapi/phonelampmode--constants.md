---
description: Die PHONELAMPMODE-Bitflagkonst constants beschreiben verschiedene Möglichkeiten, wie eine Smartphones-Lampe entladt werden kann.
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: PHONELAMPMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a39aa3437fa813b37bad74d9c42798d0151ea3ae17adee4dad90e19675e8db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862246"
---
# <a name="phonelampmode_-constants"></a>PHONELAMPMODE_ Konstanten

Die **PHONELAMPMODE_** bit-flag-Konstanten beschreiben verschiedene Möglichkeiten, wie die Glühlampe eines Telefons leuchtet.

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



Dieser Wert wird verwendet, um eine Taste/Lampe-Position zu beschreiben, die keine entsprechende Lampe enthält.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



Ein gebrochener Flatter ist die Superposition von Flash und Flatter.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash bedeutet langsames Ein- und Ausschalten.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



Flatter bedeutet schnell ein- und ausschalten.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



Die Lampe ist ausgeschaltet.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



Stabil bedeutet, dass die Lampe kontinuierlich leuchtet.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



Der Lampemodus ist derzeit unbekannt.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



Wink bedeutet normal rate on and off( Normalrate ein und aus).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die hochwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Wenn sich die genauen Ein- und Aus-Verhältnisse zwischen Denksätzen verschiedener Anbieter unterscheiden können, sollte die Zuordnung der tatsächlichen Beleuchtungsmuster für die meisten Smartphones zu den oben aufgeführten Werten unkompliziert sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




