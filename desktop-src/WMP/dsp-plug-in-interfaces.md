---
title: DSP-Plug-in-Schnittstellen
description: DSP-Plug-in-Schnittstellen
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player-Plug-ins, DSP-Schnittstellen
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, DSP-Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, ispecifypropertypage-Schnittstelle
- DSP-Plug-ins, Schnittstellen
- DSP-Plug-ins, ispecifypropertypage-Schnittstelle
- Schnittstellen, DSP-Plug-ins
- Ispecifypropertypage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390038"
---
# <a name="dsp-plug-in-interfaces"></a>DSP-Plug-in-Schnittstellen

Die Plug-in-Schnittstellen (Digital Signal Processing, DSP) werden verwendet, um die Datenübertragung zwischen Windows Media Player und dem-Plug-in zu verwalten. Alle DSP-Plug-Ins können optional die **ispecifypropertypage** -Schnittstelle implementieren, um eine Implementierung der Eigenschaften Seite bereitzustellen.

Zum Erstellen von DSP-Plug-ins sind die folgenden Schnittstellen erforderlich.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Imediaobject**                                         | Verwaltet den Datenaustausch mit Windows Media Player und führt digitale Signalverarbeitungsaufgaben aus. Im DirectX SDK ist eine ausführliche Dokumentation enthalten. |
| [Iwmpmediapluginregistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Verwaltet die Plug-in-Registrierung.                                                                                                                          |
| [Iwmpplug-in](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Verwaltet die Verbindung mit Windows Media Player.                                                                                                        |
| [Iwmppluginenable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Speichert, ob das Plug-in derzeit von Windows Media Player aktiviert ist.                                                                               |
| [Iwmpservices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Ruft Informationen über die aktuelle streamzeit und den streamzustand vom Player ab.                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Referenz für DSP-Plug-ins**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




