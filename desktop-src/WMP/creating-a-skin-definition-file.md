---
title: Erstellen einer Skindefinitionsdatei
description: Erstellen einer Skindefinitionsdatei
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Mobile Skins, Skindefinitionsdateien
- Skins, Skindefinitionsdateien
- Dateien für Skins, Skindefinition
- Skindefinitionsdateien,erstellen
- Erstellen von Skins, Informationen
- Erstellen von Skins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bb18289a8ed124c820e983c37ccc9fff60c5c1c2b0794e4964a8e170c84909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341600"
---
# <a name="creating-a-skin-definition-file"></a>Erstellen einer Skindefinitionsdatei

Eine Skindefinitionsdatei ist eine Textdatei, die eine Skin und alle ihre zusammengesetzten Teile definiert. Die Dateierweiterung muss SKN sein.

Jede Skindefinitionsdatei muss mit der folgenden Zeile beginnen, die die Versionsnummer der Skindatei angibt. Die folgende Tabelle zeigt Windows Media Player Versionen und die Codezeile, die verwendet werden sollten, um jede in einer Skindefinitionsdatei zu identifizieren. Obwohl einige der Zahlen in den Codezeilen nicht ihren Anforderungen folgen, sind sie korrekt, wie in der folgenden Tabelle gezeigt.



| Windows Media Player Version | Erste Zeile der Skindefinitionsdatei |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Pocket WMP Skin File v1.0\]      |
| 1.2                          | \[Pocket WMP Skin File v1.2\]      |
| 7.0                          | \[Pocket WMP Skin File v2.0\]      |
| 7.1                          | \[Pocket WMP Skin File v8.0\]      |
| 9-Serie                     | \[Pocket WMP Skin File v9.0.1\]    |
| Windows 10 Mobile                    | \[Pocket WMP Skin File v9.0.1\]    |
| 10.1 Mobile                  | \[Pocket WMP Skin File v9.0.1\]    |



 

Die Versionsnummer 9.0.1 gilt für Skins, die speziell für Windows Media Player 9-Serie oder höher erstellt wurden. Skins mit einer früheren Versionsnummer werden von Windows Media Player Serie 9 oder höher als Hochformat-Skins mit 96 DPI-Skins (Dots per Inch) geöffnet.

Die Skindefinitionsdatei besteht aus mehreren Abschnitten. Jeder Abschnitt definiert einen bestimmten Bereich der Skin. Die Abschnitte müssen in der folgenden Reihenfolge platziert werden:

1.  BESCHREIBUNG
2.  Bitmaps
3.  Video
4.  Schaltflächen
5.  Status
6.  Text
7.  Marquee
8.  Trackbars

Jeder Abschnitt beginnt mit dem Namen des Abschnitts in eckigen Klammern, z. B.:


```C++
[ Bitmaps ]

```



> [!Note]  
> Ihre Skindefinitionsdatei wird nur richtig analysiert, wenn Sie Leerzeichen zwischen den Klammern und dem Namen des Abschnitts angeben.

 

Anschließend definieren eine oder mehrere Zeilen einzelne Bilder, Schaltflächen und so weiter. Beispielsweise kann ein Bitmaps-Abschnitt Folgendes enthalten:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Es ist nicht erforderlich, die Werte in Spalten zu sortieren, aber es hilft Ihrem Code, besser lesbar zu sein. Weitere Informationen zu den einzelnen Abschnitten der Skindefinitionsdatei finden Sie in der [Skinreferenz.](skin-reference.md)

> [!Note]  
> Verwenden Sie keine Registerkarten an einer beliebigen Stelle in der Datei. Verwenden Sie stattdessen zusätzliche Leerzeichen. Dies ist sehr wichtig, da das Drücken der TAB-TASTE beim Schreiben oder Bearbeiten der Skindefinitionsdatei dazu führen kann, dass die gesamte Skin fehlschlägt. Jede Zeile muss vollständig sein und kann nicht mit einer zweiten Zeile fortgesetzt werden. Außerdem sind die Werte Region und Super für Skins veraltet, die mit Windows Media Player 10 Mobile oder höher verwendet werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skindefinitionsdatei**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





