---
title: Erstellen einer Skin-Definitionsdatei
description: Erstellen einer Skin-Definitionsdatei
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Mobile Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, erstellen
- Erstellen von Skins, Informationen zu
- Erstellen von Skins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711723"
---
# <a name="creating-a-skin-definition-file"></a>Erstellen einer Skin-Definitionsdatei

Eine Skin-Definitionsdatei ist eine Textdatei, die eine Skin und alle zusammengesetzten Teile definiert. Die Dateinamenerweiterung muss. SKN lauten.

Jede Skin-Definitionsdatei muss mit der folgenden Zeile beginnen, in der die Versionsnummer der Skin-Datei angegeben ist. In der folgenden Tabelle werden die Windows Media Player-Versionen und die Codezeile angezeigt, die zur Identifizierung der einzelnen in einer Skin-Definitionsdatei verwendet werden sollen. Obwohl einige der Zahlen in den Codezeilen nicht Ihren Erwartungen entsprechen, sind Sie richtig, wie in der folgenden Tabelle gezeigt.



| Windows Media Player-Version | Erste Zeile der Skin-Definitionsdatei |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Pocket WMP-Skin-Datei v 1.0\]      |
| 1.2                          | \[Pocket WMP-Skin-Datei v 1.2\]      |
| 7.0                          | \[Pocket WMP-Skin-Datei v 2.0\]      |
| 7.1                          | \[Pocket WMP-Skin-Datei v 8.0\]      |
| 9-Serie                     | \[Pocket WMP-Skin-Datei v 9.0.1\]    |
| Windows 10 Mobile                    | \[Pocket WMP-Skin-Datei v 9.0.1\]    |
| 10,1 Mobile                  | \[Pocket WMP-Skin-Datei v 9.0.1\]    |



 

Die Versionsnummer 9.0.1 ist für Skins vorgesehen, die speziell für Windows Media Player 9-Serie oder höher erstellt wurden. Skins mit einer früheren Versionsnummer werden von Windows Media Player 9 oder höher als Hochformat, 96 dpi-pro-Zoll-Skins (dpi) geöffnet.

Die Skin-Definitionsdatei besteht aus mehreren Abschnitten. Jeder Abschnitt definiert einen bestimmten Bereich der Skin. Die Abschnitte müssen in der folgenden Reihenfolge platziert werden:

1.  BESCHREIBUNG
2.  Bitmaps
3.  Video
4.  Schaltflächen
5.  Status
6.  Text
7.  Marquee
8.  Trackbars

Jeder Abschnitt beginnt mit dem Namen des Abschnitts in eckigen Klammern, z. b.:


```C++
[ Bitmaps ]

```



> [!Note]  
> Ihre Skin-Definitionsdatei wird nicht ordnungsgemäß analysiert, es sei denn, Sie fügen Leerzeichen zwischen den eckigen Klammern und dem Namen des Abschnitts ein.

 

Anschließend werden in einer oder mehreren Zeilen einzelne Bilder, Schaltflächen usw. definiert. Ein Bitmaps-Abschnitt könnte beispielsweise Folgendes enthalten:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Es ist nicht notwendig, die Werte in Spalten auszureihen, aber der Code wird leichter lesbar. Weitere Informationen zu den einzelnen Abschnitten der Skin-Definitionsdatei finden Sie in der [Skin-Referenz](skin-reference.md).

> [!Note]  
> Verwenden Sie Tabstopps nicht an einer beliebigen Stelle in der Datei. Verwenden Sie stattdessen zusätzliche Leerzeichen. Dies ist sehr wichtig, da das Drücken der Tab-Taste beim Schreiben oder Bearbeiten der Skin-Definitionsdatei dazu führt, dass die gesamte Skin ausfällt. Jede Zeile muss fertig sein und kann nicht auf eine zweite Zeile fortgesetzt werden. Außerdem sind die Bereiche "Region" und "Super" für Skins veraltet, die mit Windows Media Player 10 Mobile oder höher verwendet werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Definitionsdatei**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





