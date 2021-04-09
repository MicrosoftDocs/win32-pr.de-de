---
title: Zuordnung von Waveform-Audio Geräten
description: Zuordnung von Waveform-Audio Geräten
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- Multimedia-Audiodatei, Mapping von Waveform-Audiogeräte
- Audiodatei, Mapping von Waveform-Audiogeräte
- Audiokomprimierungs-Manager (ACM), Mapping von Waveform-Audiogeräte
- ACM (Audiokomprimierungs-Manager), Mapping von Waveform-Audiogeräte
- Mapping von Waveform-Audiogeräten
- Multimedia-Audiodatei, Mapper
- Audiodatei, Mapper
- Audiokomprimierungs-Manager (ACM), Mapper
- ACM (Audiokomprimierungs-Manager), Mapper
- mapper
- Wellenform-Audiodatei, Mapping von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855863"
---
# <a name="mapping-waveform-audio-devices"></a>Zuordnung von Waveform-Audio Geräten

Windows stellt eine Reihe von Standardfunktionen für Audiogeräte bereit. Diese Funktionen geben Aufrufe an Gerätetreiber aus, von denen Hardware Geräte verwaltet werden. Das System verwendet ein Modul, das als "Mapper" bezeichnet wird, um installierte Geräte zu verwalten. Der Mapper verwendet in der Treiberschnittstelle besondere Hooks, um Aufrufe abzufangen und als Vermittler zwischen dem System und den im System installierten Treibern zu fungieren. Der Mapper ist für das Abgleichen von Anwendungsanforderungen für den Zugriff auf ein Gerät mit den verfügbaren Geräten und für die Suche nach einem Gerät zuständig, das den Audioanforderungen der aktuellen Anwendung entspricht. Das System stellt Mapper für Standardtreiber Typen bereit: Waveform-Audiodaten, MIDI (Digital Interface Digital Interface) und hilfsangeräte.

Das ACM ist eine Erweiterung des grundlegenden Multimedia-Systems und wird als Mapper installiert. Dies bedeutet, dass das ACM die Treiber Schnittstellen-Mapper-Hooks für Waveform-Audiogeräte verwendet. Die Verwendung dieser Hooks ermöglicht dem ACM das Decodieren oder Codieren von Waveform-Audiodaten vor der Übergabe an oder von einem Waveform-Audiogerätetreiber. Der Unterschied zwischen dem ACM und dem Standardsystem Mapper besteht darin, dass das ACM nach einem Waveform-Audiogerät suchen kann, das ein bestimmtes Format unterstützt, oder eine Kombination aus einem Waveform-Audiogerät und einem ACM-Kompressor oder Dekompressor suchen kann, der ein bestimmtes Format unterstützt.

Wenn eine Anwendung anfordert, dass das System ein Waveform-Audiogerät für die Eingabe oder die Ausgabe öffnet, gibt die Anforderung das Format und das Gerät an. Wenn das angegebene Gerät der Mapper ist, muss der Mapper ein Gerät suchen, das das angegebene Format unterstützt. Der im ACM implementierte Mapper sucht nach einem installierten Waveform-Audiogerät, das das angegebene Format unterstützt. Wenn das ACM ein solches Gerät nicht finden kann, sucht es nach einem Waveform-Audiogerät und einem Kompressor oder Dekompressor, von dem das Format unterstützt wird. Insbesondere sucht das ACM nach einem Kompressor oder Dekompressor, der das angegebene Format in ein Format konvertiert, das von einem installierten Waveform-Audiogerät unterstützt wird. Nachdem das ACM ein Gerät gefunden hat, das das konvertierte Format unterstützt, kann es Anforderungen zur Wiedergabe oder Aufzeichnung des ursprünglich angeforderten Formats berücksichtigen, obwohl dieses Format von keinem installierten Waveform-Audiogerät direkt unterstützt wird.

Zusätzlich zur Formatkonvertierung bietet das ACM auch Dienste für die Unterstützung von Komprimierung, Dekomprimierung, Filterung, Format Auswahl und Filter Auswahl. Sie stellt eine Standard-API bereit, die Sie unterstützt, indem Sie Ihre eigenen Treiber aufrufen.

 

 




