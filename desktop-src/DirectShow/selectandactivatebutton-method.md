---
description: Die selectandactivatebutton-Methode wählt die angegebene Schaltfläche aus und aktiviert Sie.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Selectandactivatebutton-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346187"
---
# <a name="selectandactivatebutton-method"></a>Selectandactivatebutton-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectAndActivateButton` -Methode wählt die angegebene Schaltfläche aus und aktiviert Sie.

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Gibt die Schaltfläche als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.

Mit dieser Methode wird die angegebene Schaltfläche hervorgehoben und automatisch aktiviert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Buttonsavailable**](buttonsavailable-property.md)
</dt> <dt>

[**Currentbutton**](currentbutton-property.md)
</dt> <dt>

[**Activatebutton**](activatebutton-method.md)
</dt> <dt>

[**Getbuttonatposition**](getbuttonatposition-method.md)
</dt> <dt>

[**Getbuttonrect**](getbuttonrect-method.md)
</dt> <dt>

[**Selectatposition**](selectatposition-method.md)
</dt> </dl>

 

 



