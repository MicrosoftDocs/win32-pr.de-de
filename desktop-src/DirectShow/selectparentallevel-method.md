---
description: Die SelectParentalLevel-Methode legt die angegebene Jugendebene für die nachfolgende Wiedergabe fest.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: SelectParentalLevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95de7e8cbf1fb6fa284eddefa1ba07ebb9268825116fdac9c97fbd5d42bac84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684040"
---
# <a name="selectparentallevel-method"></a>SelectParentalLevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectParentalLevel` -Methode legt die angegebene Jugendebene für die nachfolgende Wiedergabe fest.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Gibt die Ebene der Elternverwaltung als ganze Zahl an. Um die Elternverwaltung zu aktivieren, muss *der iLevel-Parameter* zwischen 1 und 8 liegen. Um die Elternverwaltung zu deaktivieren, legen *Sie iLevel* auf -1 fest.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den aktuellen Benutzer als Zeichenfolge an. (Derzeit ignoriert.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt das Kennwort an, das derzeit in der Registrierung als Zeichenfolge gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Methode legt die Zugriffsebene im MSWebDVD-Objekt fest, die bestimmt, welche Inhalte der Benutzer wieder geben kann. Höhere Ebenen können Inhalte auf niedrigerer Ebene wieder geben, aber niedrigere Ebenen können keine Inhalte auf höherer Ebene wieder geben. Die genaue Bedeutung der acht Dvd-Elternverwaltungsebenen variiert je nach Land/Region. In den USA und Kanada werden die Ebenen den MpAA-Bewertungskategorien (Motion Picture Association of America) zugeordnet. Die Elternverwaltung im DVD-Navigator ist standardmäßig deaktiviert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wählen SieParentalCountry aus.**](selectparentalcountry-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



