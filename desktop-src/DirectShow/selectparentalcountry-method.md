---
description: Die SelectParentalCountry-Methode legt das angegebene Land bzw. die region der Eltern für die nachfolgende Wiedergabe fest.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: SelectParentalCountry-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d148145f2c38cdb01da209e02f6400301da851e1d2b41e5adaf84b2338ad21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684060"
---
# <a name="selectparentalcountry-method"></a>SelectParentalCountry-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectParentalCountry` -Methode legt das angegebene Land bzw. die angegebene Region der Eltern für die nachfolgende Wiedergabe fest.

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Gibt das Land/die Region als ganze Zahl an.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den aktuell angemeldeten Benutzer als Zeichenfolge an. (Derzeit ignoriert.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt die Anwendungskennwortzeichenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Land/die Region der Eltern bestimmt, wie die Ebenen der Eltern interpretiert werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wählen SieParentalLevel aus.**](selectparentallevel-method.md)
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

 

 



