---
description: Die NotifyParentalLevelChange-Methode aktiviert oder deaktiviert die Ereignisbehandlung für temporäre Befehle auf Der Ebene der Elternverwaltung.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: NotifyParentalLevelChange-Methode (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8382b52f64d4196b0ef74e5f3285e9bb047a4e1f77d3b0e5bec4da218ee753b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997360"
---
# <a name="notifyparentallevelchange-method"></a>NotifyParentalLevelChange-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Methode aktiviert oder deaktiviert die Ereignisbehandlung für temporäre Befehle auf Der Ebene der `NotifyParentalLevelChange` Elternverwaltung.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Gibt einen booleschen Wert an, der angibt, ob die Anwendung benachrichtigt wird, wenn das MSWebDVD-Objekt Videosegmente mit einer restriktiveren Bewertung als die Gesamtbewertung für den Datenträger trifft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Benachrichtigungen zur Elternverwaltung sind standardmäßig deaktiviert. Dies bedeutet, dass temporäre Jugendbefehle vom Datenträger zulässig sind, aber ignoriert werden und der Datenträger ohne Unterbrechung abspielt. Rufen Sie diese Methode während der Initialisierung Ihrer Anwendung auf, wenn Sie temporäre Befehle der Verwaltungsebene der Eltern vom Datenträger verarbeiten müssen. Um die Elternverwaltung nach der Aktivierung zu deaktivieren, rufen Sie diese Methode mit dem Argument false auf. Weitere Informationen zur Verwaltung von Eltern finden Sie unter [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wählen SieParentalLevel aus.**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**Wählen SieParentalCountry aus.**](selectparentalcountry-method.md)
</dt> </dl>

 

 




