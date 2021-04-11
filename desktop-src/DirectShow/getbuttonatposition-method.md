---
description: Die getbuttonatposition-Methode ruft die Nummer der Schaltfläche an den angegebenen Koordinaten ab, ohne sie auszuwählen oder zu aktivieren.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Getbuttonatposition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123536"
---
# <a name="getbuttonatposition-method"></a>Getbuttonatposition-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetButtonAtPosition` Methode ruft die Nummer der Schaltfläche an den angegebenen Koordinaten ab, ohne sie auszuwählen oder zu aktivieren.

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*
</dt> <dd>

Gibt die x-Koordinate des Mauszeigers als Ganzzahl an.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*
</dt> <dd>

Gibt die y-Koordinate des Mauszeigers als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Schaltfläche an der angegebenen Position angibt, sofern vorhanden.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt 0 (null) zurück, wenn keine Schaltfläche an den angegebenen Koordinaten vorhanden ist. Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Activatebutton**](activatebutton-method.md)
</dt> <dt>

[**Buttonsavailable**](buttonsavailable-property.md)
</dt> <dt>

[**Currentbutton**](currentbutton-property.md)
</dt> <dt>

[**Getbuttonrect**](getbuttonrect-method.md)
</dt> <dt>

[**Selectandactivatebutton**](selectandactivatebutton-method.md)
</dt> <dt>

[**Selectatposition**](selectatposition-method.md)
</dt> </dl>

 

 



