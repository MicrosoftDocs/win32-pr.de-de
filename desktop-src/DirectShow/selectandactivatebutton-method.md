---
description: Die SelectAndActivateButton-Methode wählt die angegebene Schaltfläche aus und aktiviert sie.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: SelectAndActivateButton-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d141616356db5daf2ebcb19579b924f6d4cab956e03d876d0254666d55b5702b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951909"
---
# <a name="selectandactivatebutton-method"></a>SelectAndActivateButton-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectAndActivateButton` -Methode wählt die angegebene Schaltfläche aus und aktiviert sie.

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*Ibutton*
</dt> <dd>

Gibt die Schaltfläche als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, wenn Sie eine benutzerdefinierte Mausbehandlung implementieren, nachdem [**Sie DisableAutoMouseProcessing auf**](disableautomouseprocessing-property.md) **TRUE festlegen.**

Diese Methode hebt die angegebene Schaltfläche hervor und aktiviert sie automatisch.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schaltflächen Verfügbar**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



