---
description: Die AcceptParentalLevelChange-Methode akzeptiert oder lehnt die neue temporäre Verwaltungsebene der Eltern ab.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: AcceptParentalLevelChange-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4742622ce9a2c65cdce660a8bae7fab6f84171d6bd61cdf88475c2bcd788c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873590"
---
# <a name="acceptparentallevelchange-method"></a>AcceptParentalLevelChange-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die AcceptParentalLevelChange-Methode akzeptiert oder lehnt die neue temporäre Verwaltungsebene der Eltern ab.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

Gibt die neue Elternebene als booleschen Wert an.



| Wert | BESCHREIBUNG                               |
|-------|-------------------------------------------|
| true  | Akzeptieren Sie die neue Ebene der Elternverwaltung. |
| false | Lehnen Sie die neue Ebene der Elternverwaltung ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode als Reaktion auf eine EC \_ \_ DVD-Benachrichtigung über DIE BENACHRICHTIGUNG ÜBER DEN DVD-WERTÄNDERUNG auf, um anzugeben, ob der \_ DVD-Navigator den Inhalt mit der neuen Elternebene wiedergibt, oder ob der Branch angibt, ob die neue Ebene abgelehnt \_ wird.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Erzwingen von Jugendverwaltungsebenen](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**Wählen SieParentalCountry aus.**](selectparentalcountry-method.md)
</dt> <dt>

[**Wählen SieParentalLevel aus.**](selectparentallevel-method.md)
</dt> </dl>

 

 



