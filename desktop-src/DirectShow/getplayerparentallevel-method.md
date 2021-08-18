---
description: GetPlayerParentalLevel ruft die im MSWebDVD-Objekt festgelegte Ebene der Elternverwaltung ab.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: GetPlayerParentalLevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0426c48589449e03b78d894300ff2c83d83d625a269b19f0e985f78d49973f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756480"
---
# <a name="getplayerparentallevel-method"></a>GetPlayerParentalLevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

`GetPlayerParentalLevel`Ruft die im **MSWebDVD-Objekt** festgelegte Ebene der Elternverwaltung ab.

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die aktuelle übergeordnete Ebene im DVD-Navigator angibt, oder -1, wenn die Verwaltung der Eltern deaktiviert ist.

## <a name="remarks"></a>Hinweise

Eine Playeranwendung ist für die Erzwingung der Jugendschutzmaßnahmen verantwortlich. Die Spielerelternebene ist ein von einer Anwendung festgelegter Wert, der verwendet werden kann, um die höchste Ebene der Eltern anzugeben, die der aktuelle Benutzer anzeigen kann. Wenn der DVD-Navigator auf eine neue Elternebene trifft, verwenden Sie diese Methode, um zu bestimmen, ob die neue Ebene größer als die Ebene ist, die von der Anwendung über [**SelectParentalLevel**](selectparentallevel-method.md)festgelegt wurde.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**Wählen SieParentalCountry aus.**](selectparentalcountry-method.md)
</dt> <dt>

[**Wählen SieParentalLevel aus.**](selectparentallevel-method.md)
</dt> </dl>

 

 



