---
description: Die ActivateAtPosition-Methode aktiviert die Menüschaltfläche an der angegebenen Position.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: ActivateAtPosition-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fee8b81c10b010132d07ac4418f273be228595bab45e86ec03c7828d78ba74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873550"
---
# <a name="activateatposition-method"></a>ActivateAtPosition-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die ActivateAtPosition-Methode aktiviert die Menüschaltfläche an der angegebenen Position.

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Gibt die x-Koordinate als ganze Zahl an.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Gibt die y-Koordinate als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, wenn Sie eine benutzerdefinierte Mausbehandlung implementieren, nachdem [**Sie DisableAutoMouseProcessing auf**](disableautomouseprocessing-property.md) **TRUE festlegen.**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schaltflächen Verfügbar**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



