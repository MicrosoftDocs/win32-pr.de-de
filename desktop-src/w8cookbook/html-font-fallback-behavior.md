---
title: HTML-Schriftart-Fall Back-Verhalten
description: HTML-Schriftart-Fall Back-Verhalten
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106338501"
---
# <a name="html-font-fallback-behavior"></a>HTML-Schriftart-Fall Back-Verhalten

## <a name="platform"></a>Plattform

Clients-* * Windows 8.1  
**Server:** Windows Server 2012 R2  


## <a name="description"></a>BESCHREIBUNG

Microsoft aktualisiert die Logik für UI-Schriftarten für verschiedene Sprachen in Windows Store-Apps mit HTML. Anstatt eine einzelne Schriftart für alle Sprachen zu verwenden, wird die Benutzeroberflächen Schriftart nun pro Sprache bestimmt. Beispielsweise werden UI-Schriftarten für Japanisch nun in apps, die HTML verwenden, in der Benutzeroberfläche "meiryo" angezeigt.

## <a name="manifestation"></a>Ausstrahlung

Apps, die von einer alten Schriftart abhängen, können anders aussehen. während Ihre APP-Darstellung aufgrund lesbarer Schriftarten insgesamt verbessert wird, kann es ein Problem mit Layouts geben, die von Pixel-perfekten Inhalts Größen abhängen. Beispielsweise sind einige Inhalts Zeilen möglicherweise größer als zuvor, was unerwartete Zeilenumbrüche und/oder die Größe von Container Elementen verursacht hat. In der Praxis wurden jedoch keine Probleme mit vorhandenen apps festgestellt.

## <a name="solution"></a>Lösung

Betroffene Apps können dieses Verhalten mindern, indem Sie eine bestimmte Schriftart über CSS angeben (z. b. "Font-Family: meiryo UI"), anstatt sich auf die alten Standard Schriftarten zu verlassen. In der folgenden Tabelle ist die Benutzeroberflächen Schriftart für jeden der Skriptnamen enthalten.



| Skriptname        | Benutzeroberflächen Schriftart               |
|--------------------|-----------------------|
| Arabisch             | Segoe UI              |
| Armenisch           | Segoe UI              |
| Bengali            | Nirmala UI            |
| Bopomofo           | Microsoft JhengHei UI |
| Braille            | Segoe UI Symbol       |
| Buginesisch           | Leelawadee UI         |
| Kanadische Silben | Gadugi                |
| Cherokee           | Gadugi                |
| Koptisch             | Segoe UI Symbol       |
| Han (vereinfacht)   | Microsoft YaHei UI    |
| Han (traditionell)  | Microsoft JhengHei UI |
| Kyrillisch           | Segoe UI              |
| Devanagari         | Nirmala UI            |
| Deseret            | Segoe UI Symbol       |
| Ethiopic           | Ebrima                |
| Georgisch           | Segoe UI              |
| Glagolitisch         | Segoe UI Symbol       |
| Go             | Segoe UI Symbol       |
| Griechisch              | Segoe UI              |
| Gujarati           | Nirmala UI            |
| Gurmukhi           | Nirmala UI            |
| Hebräisch             | Segoe UI              |
| Alte kursiv Formatierung         | Segoe UI Symbol       |
| Javanisch           | Javanese-Text         |
| Japanisch           | Meiryo-Benutzeroberfläche             |
| Kannada            | Mirmala-Benutzeroberfläche            |
| Khmer              | Leelawadee UI         |
| Koreanisch             | Malgun Gothic         |
| Laotisch                | Leelawadee            |
| Lateinisch              | Segoe UI              |
| Malayalam          | Nirmala UI            |
| Mongolisch          | Mongolisches Baiti       |
| Myanmar            | Myanmar Text          |
| N ' Ko               | Ebrima                |
| Ogam              | Segoe UI Symbol       |
| Ol Chiki           | Nirmala UI            |
| Altes Turkisch         | Segoe UI Symbol       |
| Oriya              | Nirmala UI            |
| Osmanya            | Ebrima                |
| Phags-pa           | Microsoft PhagsPa     |
| Runisch              | Segoe UI Symbol       |
| Sora sompg       | Nirmala UI            |
| Singhalesisch            | Nirmala UI            |
| Syrisch             | Estrangelo Edessa     |
| Tai-Le             | Microsoft Tai Le      |
| Neue Tai-Lue        | Microsoft Neu-Tai-Lue |
| Tamilisch              | Nirmala UI            |
| Telugu             | Nirmala UI            |
| Tifinagh           | Ebrima                |
| Thaana             | MV Boli               |
| Thailändisch               | Leelawadee UI         |
| Tibetisch            | Microsoft Himalaya    |
| Vai                | Ebrima                |
| Yi                 | Microsoft Yi Baiti    |



 

 

 




