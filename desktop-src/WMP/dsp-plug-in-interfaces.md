---
title: DSP-Plug-In-Schnittstellen
description: DSP-Plug-In-Schnittstellen
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player-Plug-Ins, DSP-Schnittstellen
- Windows Media Player-Plug-Ins,Schnittstellen
- Plug-Ins, DSP-Schnittstellen
- Plug-Ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, ISpecifyPropertyPage-Schnittstelle
- DSP-Plug-Ins, Schnittstellen
- DSP-Plug-Ins, ISpecifyPropertyPage-Schnittstelle
- Schnittstellen,DSP-Plug-Ins
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bd030b09377adfe965698d6c411f1a39a745979f2db2eae9f0c613cad843d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863370"
---
# <a name="dsp-plug-in-interfaces"></a>DSP-Plug-In-Schnittstellen

Die DSP-Plug-In-Schnittstellen (Digital Signal Processing, digitale Signalverarbeitung) werden verwendet, um die Datenübertragung zwischen Windows Media Player und dem Plug-In zu verwalten. Alle DSP-Plug-Ins können optional die **ISpecifyPropertyPage-Schnittstelle** implementieren, um eine Implementierung der Eigenschaftenseite zu ermöglichen.

Die folgenden Schnittstellen sind zum Erstellen von DSP-Plug-Ins erforderlich.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Verwaltet den Datenaustausch mit Windows Media Player und führt Aufgaben zur Verarbeitung digitaler Signale aus. Die ausführliche Dokumentation ist im DirectX SDK enthalten. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Verwaltet die Plug-In-Registrierung.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Verwaltet die Verbindung mit Windows Media Player.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Speichert, ob das Plug-In derzeit von der Windows Media Player.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Ruft Informationen zum aktuellen Streamzeit- und Datenstromzustand aus dem Player ab.                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierreferenz für DSP-Plug-Ins**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




