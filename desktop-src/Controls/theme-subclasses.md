---
title: Verwenden von Design Unterklassen
description: Designklassen, die Steuerelemente wie ComboBox, Edit, explorbild, Rebar, Tab und Toolbar darstellen, können untergeordnet werden, um Design Variationen für das jeweilige Steuerelement bereitzustellen.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710049"
---
# <a name="using-theme-subclasses"></a>Verwenden von Design Unterklassen

Designklassen, die Steuerelemente wie ComboBox, Edit, explorbild, Rebar, Tab und Toolbar darstellen, können untergeordnet werden, um Design Variationen für das jeweilige Steuerelement bereitzustellen. Beispielsweise wird die **Schalt** Flächen Klasse als subklassifiziert, um `Start::Button` die Steuerung über das auf die Schaltfläche **Start** angewendete Design bereitzustellen.

> [!Note]  
> Verwenden Sie beim Erstellen von Unterklassen, die in diesem Thema erläutert werden, Vorsicht. Da Unterklassen in nachfolgenden Versionen von Windows möglicherweise geändert werden oder nicht verfügbar sind, wird davon abgeraten, Sie zu verwenden.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Zwei Möglichkeiten zur Verwendung einer Design Unterklasse

Eine Anwendung kann ein untergeordnetes Design auf eine der beiden folgenden Arten verwenden:

-   Die [**openfomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) -Funktion kann mit einer Zeichenfolge in der Form `subclass::class` im *pszclasslist* -Parameter verwendet werden.
-   Sie kann [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) mit dem Design Unterklassen Namen im *pszSubAppName* -Parameter aufrufen.

## <a name="using-theme-messages-that-set-visual-style"></a>Verwenden von Design Meldungen zum Festlegen des visuellen Stils

Bestimmte Steuerelemente, wie z. b. Info Leiste und Symbolleiste, stellen bestimmte Meldungen bereit, die Sie senden können, um das Steuerelement anzuweisen, eine Design Unterklasse zu verwenden Geben Sie für diese Steuerelemente einen Zeiger auf einen Puffer an, der den Design Unterklassen Namen im *LPARAM* -Parameter der Nachricht enthält. Verwenden Sie die generische [**ccm- \_ SetWindowTheme**](ccm-setwindowtheme.md) -Nachricht, oder verwenden Sie eine bestimmte Variante, wie in der folgenden Tabelle gezeigt.



| Control    | `Message`                                             |
|------------|-----------------------------------------------------|
| QuickInfo    | [**TTM \_ SetWindowTheme**](ttm-setwindowtheme.md)   |
| Symbolleiste    | [**TB \_ SetWindowTheme**](tb-setwindowtheme.md)     |
| Grund leisten      | [**RB \_ SetWindowTheme**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SetWindowTheme**](cbem-setwindowtheme.md) |



 

In der folgenden Tabelle sind einige der Unterklassen aufgelistet, die von Windows Vista definiert werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Klasse</th>
<th>Unterklassen von  werden erstellt.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kombinationsfeld</td>
<td><ul>
<li>Adresse</li>
<li>Adressierte adressierte</li>
<li>Inactiveaddress</li>
<li>Inactiveaddresscomposited</li>
<li>Maxaddress</li>
<li>Maxaddresscomposited</li>
<li>Maxinactiveaddress</li>
<li>Maxinactiveaddresscomposited</li>
</ul></td>
</tr>
<tr class="even">
<td>Bearbeiten</td>
<td><ul>
<li>Adresse</li>
<li>Adressierte adressierte</li>
<li>Inactiveaddress</li>
<li>Inactiveaddresscomposited</li>
<li>Inactivesearchboxedit</li>
<li>Inactivesearchboxeditcomposited</li>
<li>Maxaddress</li>
<li>Maxaddresscomposited</li>
<li>Maxinactiveaddress</li>
<li>Maxinactiveaddresscomposited</li>
<li>Maxinactivesearchboxedit</li>
<li>Maxinactivesearchboxeditcomposited</li>
<li>Maxsearchboxedit</li>
<li>Maxsearchboxeditcomposited</li>
<li>Searchboxedit</li>
<li>Searchboxeditcomposited</li>
</ul></td>
</tr>
<tr class="odd">
<td>Grund leisten</td>
<td><ul>
<li>Browsertabbar</li>
<li>Inactivenavbar</li>
<li>Inactivenavbarcomposited</li>
<li>Maxinactivenavbar</li>
<li>Maxinactivenavbarcomposited</li>
<li>Maxnavbar</li>
<li>Maxnavbarcomposited</li>
<li>Navigationsleiste</li>
<li>Navbarcomposited</li>
<li>Navbarnontopmost</li>
</ul></td>
</tr>
<tr class="even">
<td>Registerkarte</td>
<td><ul>
<li>Browsertab</li>
</ul></td>
</tr>
<tr class="odd">
<td>Symbolleiste</td>
<td><ul>
<li>Go</li>
<li>Gocomposited</li>
<li>Inactivego</li>
<li>Inactivegocomposited</li>
<li>Maxgo</li>
<li>Maxgocomposited</li>
<li>Maxinactivego</li>
<li>Maxinactivegocomposited</li>
<li>SearchButton</li>
<li>Searchbuttoncomposited</li>
<li>Reise</li>
<li>Travelcomposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a>Internet Explorer-Unterklassen

In Windows Vista sind die Unterklassen bestimmter Klassen, die sich in Windows Internet Explorer und Windows Explorer befinden, auch dann verfügbar, wenn es sich nicht um die Klassen selbst handelt. In der folgenden Tabelle sind die verfügbaren Unterklassen aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Addressband</td>
<td><ul>
<li>AB</li>
<li>Abgrün</li>
<li>Abgreencomposited</li>
<li>ABrot</li>
<li>Abredcomposited</li>
<li>Abgelb</li>
<li>Abgelb zusammengesetzt</li>
</ul></td>
</tr>
<tr class="even">
<td>SearchBox</td>
<td><ul>
<li>Inactivesearchbox</li>
<li>Inactivesearchboxcomposited</li>
<li>Maxinactivesearchbox</li>
<li>Maxinactivesearchboxcomposited</li>
<li>Maxsearchbox</li>
<li>Maxsearchboxcomposited</li>
<li>Searchboxcomposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

In der folgenden Tabelle sind die Besonderheiten dieser Klassen aufgeführt.



| Control     | Teil         | Zustände                                                 |
|-------------|--------------|--------------------------------------------------------|
| Addressband | Abbackground | Normal (0x1), Hot (0x2), deaktiviert (0x3), fokussiert (0x4) |
| SEARCHBOX   | Sbbackground | Normal (0x1), Hot (0x2), deaktiviert (0x3), fokussiert (0x4) |



 

 

 




