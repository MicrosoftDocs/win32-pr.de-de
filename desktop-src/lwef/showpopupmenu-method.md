---
title: ShowPopupMenu-Methode
description: ShowPopupMenu-Methode
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339795"
---
# <a name="showpopupmenu-method"></a>ShowPopupMenu-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Zeigt das Popup Menü des Zeichens an der angegebenen Position an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Büros. ***Zeichen ("*** Merkmal-ID ***"). ShowPopupMenu*** x, y*



| Teil | BESCHREIBUNG                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Erforderlich. Ein ganzzahliger Wert, der die horizontale (*x*) Bildschirm Koordinate angibt, mit der das Menü angezeigt wird. Diese Koordinaten müssen in Pixel angegeben werden. |
| *y*  | Erforderlich. Ein *ganzzahliger* Wert, der die vertikale Bildschirm Koordinate (y) angibt, mit der das Menü angezeigt wird. Diese Koordinaten müssen in Pixel angegeben werden.   |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der-Agent zeigt automatisch das Popup Menü des Zeichens an, wenn der Benutzer mit der rechten Maustaste auf das Zeichen klickt. Wenn Sie [**autopopupmenu**](autopopupmenu-property.md) auf **false** festlegen, können Sie mit dieser Methode das Menü anzeigen.

Das Menü wird angezeigt, bis der Benutzer einen Befehl auswählt oder ein anderes Menü anzeigt. Es kann jeweils nur ein Popup Menü angezeigt werden. Daher wird durch Aufrufe dieser Methode das erste Menü abgebrochen (entfernt).

Diese Methode sollte nur aufgerufen werden, wenn die Client Anwendung der aktive Client des Zeichens ist. Andernfalls tritt ein Fehler auf. Um den Erfolg dieser Methode zu ermitteln, können Sie Sie als Funktion und einen booleschen Wert zurückgeben, der angibt, ob die Methode erfolgreich war.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Weitere Informationen

[**Autopopupmenu (Eigenschaft)**](autopopupmenu-property.md)


 

 




