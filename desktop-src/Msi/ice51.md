---
description: ICE51 überprüft, ob ein Titel für Schriftartressourcendateien bereitgestellt wurde.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1187ad79aa23ca26ade28ecf92e6cde60beb9c8cc56540bec85f2ab1ae467f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763890"
---
# <a name="ice51"></a>ICE51

ICE51 überprüft, ob ein Titel für Schriftartressourcendateien bereitgestellt wurde.

Sie müssen einen Titel für eine Schriftartressource angeben, die keinen eingebetteten Namen hat. Nur TTC-, TTF- und OTF-Schriftartressourcendateien erfordern keinen Titel, da diese Dateien einen eingebetteten Namen enthalten. Geben Sie keinen Titel für eine Schriftartressource an, die einen eingebetteten Namen enthält, da das System die Schriftart dann zweimal registriert.

**[Windows Installer 4.5 und früher:](not-supported-in-windows-installer-4-5.md)** ICE51 überprüft keine .otf-Schriftartressourcendateien.

## <a name="result"></a>Ergebnis

ICE51 gibt einen Fehler aus, wenn TTC-, TTF- und OTF-Schriftartressourcendateien mit Titeln enthalten sind. ICE51 gibt eine Warnung aus, wenn andere Schriftartressourcendateien ohne Titel enthalten sind.

## <a name="example"></a>Beispiel

ICE51 würde die folgende Warnung für das gezeigte Beispiel melden.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 würde die folgende Fehlermeldung für das gezeigte Beispiel melden.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Dateitabelle](file-table.md) (partiell)



| Datei  | FileName  |
|-------|-----------|
| Font1 | font1.ttf |
| Font2 | font2.fon |



 

[Schriftarttabelle](font-table.md)



| Datei\_ | FontTitle          |
|--------|--------------------|
| Font1  | Eine wirklich kalte Schriftart |
| Font2  |                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



