---
title: ShowPopupMenu-Methode
description: ShowPopupMenu-Methode
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cfd080adcf0158a628f019b4d48be5cd10b9c5b47d7a4b71ccd2393ad83ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600990"
---
# <a name="showpopupmenu-method"></a>ShowPopupMenu-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Zeigt das Popupmenü des Zeichens an der angegebenen Position an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). ShowPopupMenu_ * _x, y_



| Teil | Beschreibung                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Erforderlich. Ein ganzzahliger Wert, der die horizontale Bildschirmkoordinate *(x)* zum Anzeigen des Menüs angibt. Diese Koordinaten müssen in Pixel angegeben werden. |
| *y*  | Erforderlich. Ein ganzzahliger Wert, der die vertikale Bildschirmkoordinate *(y)* zum Anzeigen des Menüs angibt. Diese Koordinaten müssen in Pixel angegeben werden.   |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Agent zeigt automatisch das Popupmenü des Zeichens an, wenn der Benutzer mit der rechten Maustaste auf das Zeichen klickt. Wenn Sie [**AutoPopupMenu**](autopopupmenu-property.md) auf **False** festlegen, können Sie diese Methode verwenden, um das Menü anzuzeigen.

Das Menü bleibt so lange angezeigt, bis der Benutzer einen Befehl auswählt oder ein anderes Menü anzeigt. Es kann jeweils nur ein Popupmenü angezeigt werden. Daher werden Aufrufe dieser Methode das vorherige Menü abbrechen (entfernen).

Diese Methode sollte nur aufgerufen werden, wenn Ihre Clientanwendung der aktive Client des Zeichens ist. andernfalls schlägt der Fehler fehl. Um den Erfolg dieser Methode zu bestimmen, können Sie sie als Funktion aufrufen und einen booleschen Wert zurückgeben, der angibt, ob die Methode erfolgreich war.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Weitere Informationen

[**AutoPopupMenu-Eigenschaft**](autopopupmenu-property.md)


 

 




