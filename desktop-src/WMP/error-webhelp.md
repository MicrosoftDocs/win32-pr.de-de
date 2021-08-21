---
title: Error.webHelp-Methode
description: Die webHelp-Methode startet die Windows Media Player Webhilfeseite, um weitere Informationen zum ersten Fehler in der Fehlerwarteschlange (Index 0) anzuzeigen. | Error.webHelp-Methode
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- webHelp-Methode Windows Media Player
- webHelp-Methode Windows Media Player , Error-Klasse
- Error-Klasse Windows Media Player , webHelp-Methode
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
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577874"
---
# <a name="errorwebhelp-method"></a>Error.webHelp-Methode

Die **webHelp-Methode** startet die Windows Media Player Webhilfeseite, um weitere Informationen zum ersten Fehler in der Fehlerwarteschlange (Index 0) anzuzeigen.

## <a name="syntax"></a>Syntax


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Webhilfeseiten enthalten immer die neuesten und detailliertesten Informationen zu Windows Media Player Fehlern. Diese Methode überträgt automatisch die anderen informationen, die von der Webhilfe benötigt werden, z. B. die verwendete Betriebssystemversion.

Um direkt auf die Webhilfeseiten zuzugreifen, verwenden Sie den folgenden Fehlercode und Supportcenterlinks.

-   [Windows Media Player Fehlercodeinformationen](https://support.microsoft.com/kb/886273)
-   [Windows Media Player Solution Center](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt aber nicht den beabsichtigten Vorgang aus.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das die Microsoft Windows Media Player-Webhilfeseite startet. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Error-Objekt**](error-object.md)
</dt> </dl>

 

 





