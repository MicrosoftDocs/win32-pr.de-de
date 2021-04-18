---
title: Network. Framerate
description: Die Framerate-Eigenschaft ruft die aktuelle Video Frame Rate in Frames pro hundert Sekunden ab. Der Wert 2998 gibt z. b. 29,98 Frames pro Sekunde an.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network. Framerate-Windows-Media Player
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
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361315"
---
# <a name="networkframerate"></a>Network. Framerate

Die **Framerate** -Eigenschaft ruft die aktuelle Video Frame Rate in Frames pro hundert Sekunden ab. Der Wert 2998 gibt z. b. 29,98 Frames pro Sekunde an.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **Framerate**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **Framerate** , um die aktuelle Framerate anzuzeigen. Die Informationen werden in einem HTML-div-Code angezeigt, der mit ID = "fr" erstellt wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Network. Encode dframerate**](network-encodedframerate.md)
</dt> </dl>

 

 





