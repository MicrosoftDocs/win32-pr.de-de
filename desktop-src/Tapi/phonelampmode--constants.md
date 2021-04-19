---
description: Die Bit-Flag-Konstanten von phonelampmode beschreiben verschiedene Methoden, mit denen ein Telefon Lamp beleuchtet werden kann.
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: PHONELAMPMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8df5920df79e6fc59eb12bf1f517b4070e617d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372518"
---
# <a name="phonelampmode_-constants"></a>PHONELAMPMODE_ Konstanten

Die **PHONELAMPMODE_** Bit-Flag-Konstanten beschreiben verschiedene Methoden, mit denen die Lamp eines Telefons beleuchtet werden können.

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



Dieser Wert wird verwendet, um eine Schaltfläche/Lamp-Position zu beschreiben, die keine entsprechende Lamp hat.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



Ein fehlerhafter flutterwert ist die Superposition von Flash und Flutter.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash bedeutet, dass ein-und ausgeschaltet wird.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



Flutter bedeutet ein schnelles Ein-und ausschalten.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



Die Lamp ist deaktiviert.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



"Konstant" bedeutet, dass der Lamp kontinuierlich beleuchtet wird.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



Der Lamp-Modus ist zurzeit unbekannt.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



Wink bedeutet, dass der normale Satz ein-und ausgeschaltet ist


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Wenn sich die genauen ein-und Nachteile von Telefon Sätzen von unterschiedlichen Anbietern unterscheiden können, sollte die Zuordnung der eigentlichen Lamp-Beleuchtungs Muster für die meisten Telefone auf die oben aufgeführten Werte ganz einfach sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




