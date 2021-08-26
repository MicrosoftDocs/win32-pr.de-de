---
title: Network.frameRate
description: Die frameRate-Eigenschaft ruft die aktuelle Videobildrate in Frames pro hundert Sekunden ab. Der Wert 2998 gibt beispielsweise 29,98 Frames pro Sekunde an.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network.frameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da4a0f292c4693c263115dc1ad59ea3c71946d81838d427e6d8e043ac499709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901650"
---
# <a name="networkframerate"></a>Network.frameRate

Die **frameRate-Eigenschaft** ruft die aktuelle Videobildrate in Frames pro hundert Sekunden ab. Der Wert 2998 gibt beispielsweise 29,98 Frames pro Sekunde an.

## <a name="syntax"></a>Syntax

*Player*. *network*. **frameRate**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **frameRate,** um die aktuelle Bildfrequenz anzuzeigen. Die Informationen werden in einem HTML-DIV angezeigt, das mit der ID = "FR" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> <dt>

[**Network.encodedFrameRate**](network-encodedframerate.md)
</dt> </dl>

 

 





