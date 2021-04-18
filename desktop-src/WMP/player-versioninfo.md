---
title: Player. VERSIONINFO
description: Die VERSIONINFO-Eigenschaft ruft einen Zeichen folgen Wert ab, der die Version des Windows-Media Player angibt.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player. VERSIONINFO-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364907"
---
# <a name="playerversioninfo"></a>Player. VERSIONINFO

Die **VERSIONINFO** -Eigenschaft ruft einen Zeichen folgen Wert ab, der die Version des Windows-Media Player angibt.

## <a name="syntax"></a>Syntax

*Player* . **VERSIONINFO**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** im folgenden Format: "*X*. 0,0. *Yyyy*"Where *X* steht für die Hauptversionsnummer und *yyyy* für die Buildnummer.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das, wenn darauf geklickt wird, ein Meldungs Feld mit den Versionsinformationen für Windows Media Player anzeigt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





