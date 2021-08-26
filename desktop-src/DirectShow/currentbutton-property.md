---
description: Die CurrentButton-Eigenschaft ruft die Nummer der ausgewählten Menüschaltfläche ab.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: CurrentButton-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b246b77283a2632f2feac4c2b374075ef9d9a205bcb71813856b9847df21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053140"
---
# <a name="currentbutton-property"></a>CurrentButton-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentButton` -Eigenschaft ruft die Nummer der ausgewählten Menüschaltfläche ab.

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Schaltfläche darstellt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Verwenden Sie diese Methode, wenn Sie eine benutzerdefinierte Mausbehandlung implementieren, nachdem [**Sie DisableAutoMouseProcessing auf**](disableautomouseprocessing-property.md) **TRUE festlegen.**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**Schaltflächen Verfügbar**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



