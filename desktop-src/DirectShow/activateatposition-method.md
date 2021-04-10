---
description: Die activateatposition-Methode aktiviert die Menü Schaltfläche an der angegebenen Position.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Activateatposition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125329"
---
# <a name="activateatposition-method"></a>Activateatposition-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die activateatposition-Methode aktiviert die Menü Schaltfläche an der angegebenen Position.

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
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
</dt> <dt>

[**Selectatposition**](selectatposition-method.md)
</dt> </dl>

 

 



