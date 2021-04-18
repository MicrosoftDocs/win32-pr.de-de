---
title: Settings. stumm
description: Mit der Eigenschaft stumm wird ein Wert angegeben und abgerufen, der angibt, ob Audiodaten stumm geschaltet werden.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Einstellungen. stumm schalten von Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371086"
---
# <a name="settingsmute"></a>Settings. stumm

Mit der Eigenschaft **stumm** wird ein Wert angegeben und abgerufen, der angibt, ob Audiodaten stumm geschaltet werden.

## <a name="syntax"></a>Syntax

Player. Settings. stumm

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                  |
|-------|------------------------------|
| true  | Audiodaten werden stumm geschaltet.              |
| false | Standard. Das Audioformat wird nicht stumm geschaltet. |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Checkbox-Element erstellt, mit dem der Benutzer Audiodaten stumm schalten und die stumm Schaltung aufheben kann. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 





