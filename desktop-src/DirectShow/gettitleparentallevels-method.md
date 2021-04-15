---
description: Die gettitleparser-Methode ruft die Jugend Verwaltungsebenen für den angegebenen Titel ab.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Gettitleparser-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392622"
---
# <a name="gettitleparentallevels-method"></a>Gettitleparser-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetTitleParentalLevels` Methode ruft die Jugend Verwaltungsebenen für den angegebenen Titel ab.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*
</dt> <dd>

Gibt den Titel als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, dessen einzelne Bits angeben, welche Personen Verwaltungsebenen (PML) im angegebenen Titel festgelegt sind.

## <a name="remarks"></a>Bemerkungen

Ein Titel kann über Kapitel oder sogar kurze Segmente verfügen, deren PML von der Gesamt-PML für den Titel abweicht. Verwenden Sie diese Methode, um alle PMLs zu ermitteln, die bei der Wiedergabe eines bestimmten Titels gefunden werden. Die zurückgegebene Ganzzahl ist ein Satz von Bitflags, die wie in der folgenden Tabelle dargestellt definiert werden. Führt eine bitweise AND-Operation auf *ilevels* und jedem möglichen Wert aus. Wenn der Vorgang **true** zurückgibt, bedeutet dies, dass an einem bestimmten Punkt in diesem Titel PML angezeigt wird.



| Wert  | BESCHREIBUNG          |
|--------|----------------------|
| 0x100  | DVD-Jugend Stufe 1 |
| 0x200  | DVD-Jugend Stufe 2 |
| 0x400  | DVD-elternebene 3 |
| 0x800  | DVD-elternebene 4 |
| 0x1000 | DVD-Jugend Stufe 5 |
| 0x2000 | DVD-elternebene 6 |
| 0x4000 | DVD-Jugend Stufe 7 |
| 0x8000 | DVD-elternebene 8 |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Selectparser-allevel**](selectparentallevel-method.md)
</dt> <dt>

[**Getplayerparameentalcountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**Getplayerparser**](getplayerparentallevel-method.md)
</dt> <dt>

[**Selectpartalcountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



