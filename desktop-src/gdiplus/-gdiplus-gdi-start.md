---
description: Windows GDI+ ist eine klassenbasierte API für C/C++-Programmierer.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129068"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>Zweck

Windows GDI+ ist eine klassenbasierte API für C/C++-Programmierer. Sie ermöglicht es Anwendungen, Grafiken und formatierten Text sowohl auf der Videoanzeige als auch auf dem Drucker zu verwenden. Anwendungen, die auf der Microsoft Win32-API basieren, greifen nicht direkt auf die Grafikhardware zu. Stattdessen interagiert GDI+ im Auftrag von Anwendungen mit Gerätetreibern. GDI+ wird auch von Microsoft Win64 unterstützt.

## <a name="where-applicable"></a>Anwendungsbereich

GDI+-Funktionen und-Klassen werden nicht für die Verwendung in einem Windows-Dienst unterstützt. Der Versuch, diese Funktionen und Klassen von einem Windows-Dienst zu verwenden, kann zu unerwarteten Problemen führen, wie z. b. verminderter Dienstleistung und Lauf Zeit Ausnahmen oder-Fehler.

> [!Note]  
> Wenn Sie die GDI+-API verwenden, dürfen Sie niemals zulassen, dass Ihre Anwendung beliebige Schriftarten aus nicht vertrauenswürdigen Quellen herunterlädt. Das Betriebssystem erfordert erhöhte Berechtigungen, um sicherzustellen, dass alle installierten Schriftarten vertrauenswürdig sind.

## <a name="developer-audience"></a>Entwicklergruppe

Die klassenbasierte GDI+ C++-Schnittstelle ist für die Verwendung durch C/C++-Programmierer konzipiert. Kenntnisse über die grafische Benutzeroberfläche von Windows und die Nachrichten gesteuerte Architektur sind erforderlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

GDI+ kann in allen Windows-basierten Anwendungen verwendet werden. GDI+ wurde in Windows XP und Windows Server 2003 eingeführt. Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Klasse oder Methode erforderlich sind, finden Sie im Abschnitt Weitere Informationen in der Dokumentation für die Klasse oder Methode.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                    | BESCHREIBUNG                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [Übersicht](-gdiplus-about-gdi--about.md)<br/>     | Allgemeine Informationen zu GDI+.<br/>            |
| [Genutzt](-gdiplus-using-gdi--use.md)<br/>          | Aufgaben und Beispiele mit GDI+.<br/>             |
| [Referenz](-gdiplus-class-gdi-reference.md)<br/> | Dokumentation für die klassenbasierte API von GDI+ C++.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows GDI](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Windows-Abbild Erfassung](../wia/-wia-startpage.md)
</dt> <dt>

[OpenGL](../opengl/opengl.md)
</dt> <dt>

[Windows Multimedia](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
