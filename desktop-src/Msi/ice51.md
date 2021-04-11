---
description: ICE51 prüft, ob ein Titel für Schriftart Ressourcen Dateien bereitgestellt wurde.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217353"
---
# <a name="ice51"></a>ICE51

ICE51 prüft, ob ein Titel für Schriftart Ressourcen Dateien bereitgestellt wurde.

Sie müssen einen Titel für eine Schriftart Ressource angeben, die keinen eingebetteten Namen besitzt. Nur die Font-Ressourcen Dateien. TTC,. ttf und OTF erfordern keinen Titel, da diese Dateien einen eingebetteten Namen enthalten. Geben Sie keinen Titel für eine Schriftart Ressource an, die einen eingebetteten Namen enthält, da das System die Schriftart dann zweimal registriert.

**[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** ICE51 überprüft keine. OTF-Schriftart Ressourcen Dateien.

## <a name="result"></a>Ergebnis

ICE51 gibt einen Fehler aus, wenn die Schriftarten Ressourcen Dateien ". TTC", ". ttf" und "otf" mit Titeln vorhanden sind. ICE51 gibt eine Warnung aus, wenn andere Schriftart Ressourcen Dateien ohne Titel vorhanden sind.

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



| File  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | font2. FON |



 

[Schriftart Tabelle](font-table.md)



| Datei\_ | FontTitle          |
|--------|--------------------|
| Font1  | Eine wirklich coole Schriftart |
| Font2  |                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



