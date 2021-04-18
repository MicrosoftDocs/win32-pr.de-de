---
title: Methoden (IInertiaProcessor)
description: Dieser Abschnitt enthält die Methoden für die IInertiaProcessor-Schnittstelle.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows-Berührungs-, IInertiaProcessor-Schnittstelle
- Windows-Berührungs Schnittstellen Methoden
- Trägheit, IInertiaProcessor-Schnittstelle
- IInertiaProcessor-Schnittstelle, Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337485"
---
# <a name="methods-iinertiaprocessor"></a>Methoden (IInertiaProcessor)

Dieser Abschnitt enthält die Methoden für die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle.



| Methode                                                 | BESCHREIBUNG                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zurücksetzen**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Initialisiert den Prozessor mit dem anfänglichen Zeitstempel und startet die Trägheit neu.                                                                                                                                                    |
| [**Prozess**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Führt Berechnungen für den aktuellen Tick aus und kann je nachdem, ob die extrapolierungs Methode abgeschlossen ist, das **Delta** -oder **abgeschlossene** Ereignis erhöhen. Wenn die extrapolierungs Methode zum vorherigen Tick abgeschlossen wurde, ist die Methode No-op. |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Führt Berechnungen für den angegebenen Tick aus und kann je nachdem, ob die extrapolierungs Methode abgeschlossen ist, das **Delta** -oder **abgeschlossene** Ereignis erhöhen.                                                                        |
| [**Abgeschlossen**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Beendet die aktuelle Bearbeitung und beendet die Trägheit des trägheitprozessors.                                                                                                                                              |
| [**Completetime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Schließt die aktuelle Bearbeitung am angegebenen Tick ab, hält die Trägheit des Trägheits Prozessors an und löst das Ereignis "manipulationabgeschlossene" aus.                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




