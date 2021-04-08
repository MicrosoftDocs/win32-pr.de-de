---
description: Die selectatposition-Methode wählt die Menü Schaltfläche an den angegebenen Koordinaten des Mauszeigers aus.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Selectatposition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746249"
---
# <a name="selectatposition-method"></a>Selectatposition-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SelectAtPosition` Methode wählt die Menü Schaltfläche an den angegebenen Koordinaten des Mauszeigers aus.

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*XPos*
</dt> <dd>

Gibt die x-Koordinate als ganze Zahl an.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*YPos*
</dt> <dd>

Gibt die y-Koordinate als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.

Durch Auswahl von wird nur die Schaltfläche hervorgehoben Um den Befehl zu senden, der einer ausgewählten Schaltfläche zugeordnet ist, aufrufen Sie [**activatebutton**](activatebutton-method.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Buttonsavailable**](buttonsavailable-property.md)
</dt> <dt>

[**Currentbutton**](currentbutton-property.md)
</dt> <dt>

[**Getbuttonatposition**](getbuttonatposition-method.md)
</dt> <dt>

[**Getbuttonrect**](getbuttonrect-method.md)
</dt> <dt>

[**Selectandactivatebutton**](selectandactivatebutton-method.md)
</dt> </dl>

 

 



