---
title: Error. WebHelp-Methode
description: Die WebHelp-Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null). | Error. WebHelp-Methode
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- WebHelp-Methode (Windows Media Player)
- WebHelp-Methode, Windows Media Player, Fehler Klasse
- Error-Klasse, Windows Media Player, WebHelp-Methode
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370280"
---
# <a name="errorwebhelp-method"></a>Error. WebHelp-Methode

Die **WebHelp** -Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null).

## <a name="syntax"></a>Syntax


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Web-Hilfeseiten enthalten stets die neuesten und detailliertesten Informationen zu Windows Media Player-Fehlern. Diese Methode überträgt automatisch die anderen Informationen, die von der Webhilfe benötigt werden, z. b. die verwendete Betriebssystemversion.

Wenn Sie direkt auf die Web-Hilfeseiten zugreifen möchten, verwenden Sie die folgenden Links zu Fehlercode und Support Center.

-   [Windows Media Player-Fehler Code Informationen](https://support.microsoft.com/kb/886273)
-   [Windows Media Player-Lösungs Center](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das die Microsoft Windows Media Player-Webhilfe Seite aufruft. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Error-Objekt**](error-object.md)
</dt> </dl>

 

 





