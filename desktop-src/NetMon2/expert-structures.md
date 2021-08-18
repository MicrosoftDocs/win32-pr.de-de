---
description: Expertenhilfsfunktionen, die von Netzwerkmonitor und allgemeinen Hilfsfunktionen bereitgestellt werden, verwenden die in der folgenden Tabelle beschriebenen Strukturen.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Expertenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16accf769b0983b782a6e6dbd723dd08df27415220bda1d59122b951439bac65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939017"
---
# <a name="expert-structures"></a>Expertenstrukturen

Expertenhilfsfunktionen, die von Netzwerkmonitor und allgemeinen Hilfsfunktionen bereitgestellt werden, verwenden die in der folgenden Tabelle beschriebenen Strukturen.



| Struktur                                              | Beschreibung                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Ordnet der Konfiguration eine Experten-DLL zu.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Stellt Unformatierte Konfigurationsdaten bereit.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Stellt Informationen zur Experten-DLL bereit. Netzwerkmonitor verwendet die Informationen.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Stellt Informationen zu einem Frame bereit.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Stellt Startinformationen über den Experten bereit.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Stellt den aktuellen Status eines ausgeführten Experten bereit.                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | Definiert die Anzeigefiltermerkmale für einen Experten.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Stellt Informationen zu einer Zeile bereit, die im Expertenviewer angezeigt wird.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Stellt Informationen bereit, die eine Spalte im Ereignisanzeige definieren.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Stellt einen Container für alle möglichen Daten bereit, die in einer Zeile im Ereignisanzeige in eine Spalte eingefügt werden.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | Der Einstiegspunkt in der Variante, der angibt, welches Element der Union verwendet werden soll und wie es formatiert werden soll. |



 

Netzwerkmonitor stellt auch Exportfunktionen (Hilfsfunktionen, die der Experte aufrufen kann) und Enumerationen bereit.



| Informationen über                                          | Finden Sie unter                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Exportieren Sie Funktionen, die Einstiegspunkte für Ihre Experten-DLL bereitstellen. | [Experten-DLL-Exportfunktionen](expert-dll-export-functions.md)               |
| Hilfsfunktionen, die von Experten und Parsern aufgerufen werden können.    | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |
| Hilfsfunktionen, die nur von Experten aufgerufen werden.              | [Expertenfunktionen](expert-functions.md)                                     |
| Enumerationen, die von Expertenstrukturen und -funktionen verwendet werden.          | [Expertenenumerationen](expert-enumerations.md)                               |



 

 

 



