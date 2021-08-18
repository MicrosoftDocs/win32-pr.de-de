---
title: Player.versionInfo
description: Die versionInfo-Eigenschaft ruft einen Zeichenfolgenwert ab, der die Version des Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player.versionInfo-Windows Media Player
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
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995830"
---
# <a name="playerversioninfo"></a>Player.versionInfo

Die **versionInfo-Eigenschaft** ruft einen Zeichenfolgenwert ab, der die Version des Windows Media Player.

## <a name="syntax"></a>Syntax

*Player* . **versionInfo**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** im folgenden Format: "*X*.0.0. *YYYY*", wobei *X* die Hauptversionsnummer und *YYYY die* Buildnummer darstellt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das, wenn darauf geklickt wird, ein Meldungsfeld mit den Versionsinformationen für Windows Media Player. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





