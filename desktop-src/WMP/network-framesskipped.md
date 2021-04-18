---
title: Network. framesskipped
description: Die framesskipped-Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Netzwerk. framesskipped Windows Media Player
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
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365491"
---
# <a name="networkframesskipped"></a>Network. framesskipped

Die **framesskipped** -Eigenschaft ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **framesskipped**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **framesskipped** zum Anzeigen der Gesamtzahl der Rahmen, die während der Wiedergabe ausgelassen werden, wenn der Benutzer auf eine Schaltfläche klickt. Die Informationen werden in einem HTML-div-Code angezeigt, der mit ID = "FS" erstellt wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> </dl>

 

 





