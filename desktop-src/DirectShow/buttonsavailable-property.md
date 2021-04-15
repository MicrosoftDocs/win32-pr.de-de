---
description: Die buttonsavailable-Eigenschaft ruft die Gesamtzahl der Schaltflächen im aktuellen Menü ab.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Buttonsavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392750"
---
# <a name="buttonsavailable-property"></a>Buttonsavailable (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `ButtonsAvailable` Eigenschaft ruft die Gesamtanzahl der Schaltflächen im aktuellen Menü ab.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Integer-Wert zurück, der die Anzahl der Schaltflächen darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Verwenden Sie diese Methode, wenn Sie die benutzerdefinierte Maus Behandlung nach dem Festlegen von [**disableautomouseprocessing**](disableautomouseprocessing-property.md) auf **true** festlegen.

Rufen Sie diese Methode auf, um die Obergrenze für den Bereich gültiger Schaltflächen Nummern abzurufen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

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

 

 



