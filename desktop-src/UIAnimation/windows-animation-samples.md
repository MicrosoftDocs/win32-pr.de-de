---
title: Beispiele für Windows-Animationen
description: Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation zu Windows Animation Manager unterstützen.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animation Windows Animation Windows Animation, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310863"
---
# <a name="windows-animation-samples"></a>Beispiele für Windows-Animationen

Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation zu Windows Animation Manager unterstützen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Beispiel für eine Anwendungs gesteuerte Animation](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Beispiel für eine Zeit Geber gesteuerte Animation](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Beispiel für benutzerdefiniertes Interpolator](custom-interpolator-sample.md)<br/>                   | Zeigt, wie die Windows-Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwendet wird, wobei Direct2D zum Rendern verwendet wird. <br/> |
| [Raster Layout-Beispiel](grid-layout-sample.md)<br/>                                   | Veranschaulicht die Verwendung der Windows-Animation mit Direct2D zum Animieren eines Bild Blatts. <br/>                         |
| [Beispiel für Prioritäts Vergleich](priority-comparison-sample.md)<br/>                   | Zeigt, wie die Windows-Animation mit einem eigenen Prioritäts Vergleich verwendet wird, wobei Direct2D für das Rendering verwendet wird.<br/>      |



 

## <a name="sample-files"></a>Beispieldateien

Jedes Beispiel enthält viele der folgenden Schlüsseldateien:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp
</dt> <dd>

Definiert den Einstiegspunkt der Anwendung.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h
</dt> <dd>

Deklariert die CMainWindow-Klasse.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp
</dt> <dd>

Initialisiert die Animations Komponenten und die Grafik Plattform, lädt Bilder und rendert den Client Bereich.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>Layoutmanager. h
</dt> <dd>

Deklariert die clayoutmanager-Klasse.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>Layoutmanager. cpp
</dt> <dd>

Berechnet das Layout von Bildern im Hauptfenster, erstellt Storyboards, fügt dem Storyboard Übergänge hinzu und plant das Storyboard.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Miniaturansicht. h
</dt> <dd>

Deklariert die cminiatur-Klasse.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Miniaturansicht. cpp
</dt> <dd>

Erstellt Animations Variablen und rendert Miniaturansichten.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Leit Faden für Windows-Animationen](windows-animation-developer-guide.md)
</dt> <dt>

[Referenz zur Windows-Animation](windows-animation-reference.md)
</dt> </dl>

 

 





