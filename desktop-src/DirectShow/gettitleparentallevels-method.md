---
description: Die GetTitleParentalLevels-Methode ruft die Verwaltungsebenen der Eltern für den angegebenen Titel ab.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: GetTitleParentalLevels-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ef462767c280f5e6f1c58679a78ee876e58042dce632f30711c198b4ca574a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536670"
---
# <a name="gettitleparentallevels-method"></a>GetTitleParentalLevels-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetTitleParentalLevels` -Methode ruft die Verwaltungsebenen der Eltern für den angegebenen Titel ab.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Gibt den Titel als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, dessen einzelne Bits angeben, welche Jugendverwaltungsebenen (PML) im angegebenen Titel festgelegt sind.

## <a name="remarks"></a>Hinweise

Ein Titel kann Kapitel oder sogar kurze Segmente aufweisen, deren PML sich von der gesamten PML für den Titel unterscheidet. Verwenden Sie diese Methode, um alle PMLs zu bestimmen, die beim Wiedergeben eines angegebenen Titels auftreten. Die zurückgegebene ganze Zahl ist ein Satz von Bitflags, die wie in der folgenden Tabelle definiert sind. Führen Sie eine bitweise AND-Operation für *iLevels* und jeden möglichen Wert aus. Wenn der Vorgang **true** zurückgibt, bedeutet dies, dass PML zu einem bestimmten Zeitpunkt in diesem Titel gefunden wird.



| Wert  | Beschreibung          |
|--------|----------------------|
| 0x100  | DVD- Jugendstufe 1 |
| 0x200  | DVD- Jugendstufe 2 |
| 0x400  | DVD- Jugendstufe 3 |
| 0x800  | DVD- Jugendstufe 4 |
| 0x1000 | DVD- Jugendstufe 5 |
| 0x2000 | DVD- Jugendstufe 6 |
| 0x4000 | DVD- Jugendstufe 7 |
| 0x8000 | DVD- Jugendstufe 8 |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wählen SieParentalLevel aus.**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**Wählen SieParentalCountry aus.**](selectparentalcountry-method.md)
</dt> </dl>

 

 



