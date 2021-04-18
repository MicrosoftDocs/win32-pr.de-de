---
description: Die selectparser-allevel-Methode legt die angegebene Jugend Stufe für die nachfolgende Wiedergabe fest.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Selectparser-allevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521272"
---
# <a name="selectparentallevel-method"></a>Selectparser-allevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SelectParentalLevel` Methode legt die angegebene Jugend Stufe für die nachfolgende Wiedergabe fest.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Gibt die Jugend Verwaltungsebene als Ganzzahl an. Um die Eltern Verwaltung zu aktivieren, muss der *iLevel* -Parameter zwischen 1 und 8 liegen. Um die Jugendverwaltung zu deaktivieren, legen Sie *iLevel* auf-1 fest.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Gibt den aktuellen Benutzer als Zeichenfolge an. (Wird zurzeit ignoriert.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Gibt das Kennwort an, das zurzeit als Zeichenfolge in der Registrierung gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt die Zugriffsebene im mswebdvd-Objekt fest, das bestimmt, welche Inhalte der Benutzer wiedergeben kann. Eine höhere Ebene kann Inhalte auf niedrigerer Ebene wiedergeben, aber niedrigere Ebenen können keine Inhalte höherer Ebene wiedergeben. Die genaue Bedeutung der acht Verwaltungsebenen für die DVD ist abhängig vom Land/der Region. In den USA und Kanada werden die Ebenen der Kategorie Motion Image Association of America (MPa) Rating zugeordnet. Die Eltern Verwaltung im DVD-Navigator ist standardmäßig deaktiviert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Selectpartalcountry**](selectparentalcountry-method.md)
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

 

 



