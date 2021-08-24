---
title: Windows Animationsbeispiele
description: Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation Windows Animation Manager unterstützen.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Windows Animation Windows Animation , Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9119ab7333f1f5d74b9be9998ad26b36139f9a92d88fec856d3f4572d12f431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656150"
---
# <a name="windows-animation-samples"></a>Windows Animationsbeispiele

Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation Windows Animation Manager unterstützen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | Beschreibung                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Beispiel für anwendungsgesteuerte Animation](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Beispiel für timergesteuerte Animation](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Beispiel für benutzerdefinierten Interpolator](custom-interpolator-sample.md)<br/>                   | Zeigt, wie Sie Windows Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwenden, bei dem Direct2D für das Rendering verwendet wird. <br/> |
| [Beispiel für Rasterlayout](grid-layout-sample.md)<br/>                                   | Zeigt, wie Sie Windows Animation verwenden, indem Sie Direct2D verwenden, um ein Raster von Bildern zu animieren. <br/>                         |
| [Beispiel für einen Prioritätsvergleich](priority-comparison-sample.md)<br/>                   | Zeigt, wie Sie Windows Animation mit einem eigenen Prioritätsvergleich verwenden, indem Sie Direct2D für das Rendering verwenden.<br/>      |



 

## <a name="sample-files"></a>Beispieldateien

Jedes Beispiel enthält viele der folgenden Schlüsseldateien:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp
</dt> <dd>

Definiert den Anwendungseinstiegspunkt.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h
</dt> <dd>

Deklariert die CMainWindow-Klasse.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp
</dt> <dd>

Initialisiert die Animationskomponenten und die Grafikplattform, lädt Bilder und rendert den Clientbereich.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h
</dt> <dd>

Deklariert die CLayoutManager-Klasse.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp
</dt> <dd>

Berechnet das Layout von Bildern im Hauptfenster, erstellt Storyboards, fügt dem Storyboard Übergänge hinzu und legt das Storyboard vor.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h
</dt> <dd>

Deklariert die CThumbNail-Klasse.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp
</dt> <dd>

Erstellt Animationsvariablen und rendert Miniaturansichten.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Entwicklungshandbuch für Animationen](windows-animation-developer-guide.md)
</dt> <dt>

[Windows Animationsreferenz](windows-animation-reference.md)
</dt> </dl>

 

 





