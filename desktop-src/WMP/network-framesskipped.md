---
title: Network.framesSkipped
description: Die framesSkipped-Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Network.framesSkipped-Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1031585feae5fa2c7fdd9f5fb64bf958e77b8029d502f3e99476024276a652cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901670"
---
# <a name="networkframesskipped"></a>Network.framesSkipped

Die **framesSkipped-Eigenschaft** ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.

## <a name="syntax"></a>Syntax

*Player*. *network*. **framesSkipped**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Network* verwendet. **framesSkipped** zum Anzeigen der Gesamtanzahl von Frames, die während der Wiedergabe übersprungen wurden, wenn der Benutzer auf eine Schaltfläche klickt. Die Informationen werden in einem HTML-DIV angezeigt, das mit der ID " FS" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> </dl>

 

 





