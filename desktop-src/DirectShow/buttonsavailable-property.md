---
description: Die ButtonsAvailable-Eigenschaft ruft die Gesamtzahl der Schaltflächen im aktuellen Menü ab.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: ButtonsAvailable-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16e14675238711ef0b572477334fecba0311ca2bb54d67fc3fe012ae6d1ede9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955559"
---
# <a name="buttonsavailable-property"></a>ButtonsAvailable-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `ButtonsAvailable` -Eigenschaft ruft die Gesamtzahl der Schaltflächen im aktuellen Menü ab.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Anzahl der Schaltflächen darstellt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Verwenden Sie diese Methode, wenn Sie eine benutzerdefinierte Mausbehandlung implementieren, nachdem [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) auf TRUE festgelegt **wurde.**

Rufen Sie diese Methode auf, um die Obergrenze für den Bereich gültiger Schaltflächennummern abzurufen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

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

 

 



