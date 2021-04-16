---
description: Die selectsamentalcountry-Methode legt das angegebene jugendland/die angegebene Region für die nachfolgende Wiedergabe fest.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Selectsamentalcountry-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522179"
---
# <a name="selectparentalcountry-method"></a>Selectsamentalcountry-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SelectParentalCountry` -Methode legt das angegebene Eltern Land/die angegebene Region für nachfolgende Wiedergabe fest.

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Gibt das Land/die Region als Ganzzahl an.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den aktuell angemeldeten Benutzer als Zeichenfolge an. (Wird zurzeit ignoriert.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt die Anwendungs Kennwort-Zeichenfolge an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das elterliche Land/die Region bestimmt, wie die Jugend Stufen interpretiert werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Selectparser-allevel**](selectparentallevel-method.md)
</dt> <dt>

[**Notifyparametriallevelchange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**Gettitleparamevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**Getplayerparameentalcountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**Getplayerparser**](getplayerparentallevel-method.md)
</dt> <dt>

[**Accept-Parser-allevelchange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



