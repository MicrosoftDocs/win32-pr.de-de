---
description: Die getbuttonrect-Methode ruft das Rechteck für die angegebene Schaltfläche in Fenster Koordinaten ab.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Getbuttonrect-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123535"
---
# <a name="getbuttonrect-method"></a>Getbuttonrect-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetButtonRect` Methode ruft das Rechteck für die angegebene Schaltfläche in Fenster Koordinaten ab.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Gibt die Schaltflächen Nummer als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein [dvdrect](dvdrect-object.md) -Objekt zurück, das das Rechteck definiert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Buttonsavailable**](buttonsavailable-property.md)
</dt> <dt>

[**Currentbutton**](currentbutton-property.md)
</dt> <dt>

[**Activatebutton**](activatebutton-method.md)
</dt> <dt>

[**Selectandactivatebutton**](selectandactivatebutton-method.md)
</dt> <dt>

[**Selectatposition**](selectatposition-method.md)
</dt> </dl>

 

 



