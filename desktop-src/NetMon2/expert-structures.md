---
description: Die von Netzwerkmonitor und allgemeinen Hilfsfunktionen bereitgestellten Funktionen des expertenhilfsobjekts verwenden die in der folgenden Tabelle beschriebenen Strukturen.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Expertenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b9da00a71c3cdb9defe4396f4339f750cca359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958729"
---
# <a name="expert-structures"></a>Expertenstrukturen

Die von Netzwerkmonitor und allgemeinen Hilfsfunktionen bereitgestellten Funktionen des expertenhilfsobjekts verwenden die in der folgenden Tabelle beschriebenen Strukturen.



| Struktur                                              | BESCHREIBUNG                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Konfigurieren von "Konfigurieren"**](configuredexpert.md)           | Ordnet eine Experten-dll der Konfiguration zu.                                                       |
| [**Expertconfig**](expertconfig.md)                   | Stellt rohkonfigurations Daten bereit.                                                                       |
| [**Experteninfo**](expertenuminfo.md)               | Enthält Informationen über die Experten-dll. In Netzwerkmonitor werden die Informationen verwendet.                       |
| [**Expertframedescriptor**](expertframedescriptor.md) | Stellt Informationen zu einem Frame bereit.                                                                    |
| [**Expertstartupinfo**](expertstartupinfo.md)         | Stellt Startinformationen über den Experten bereit.                                                         |
| [**Expertenstatus**](expertstatus.md)                   | Gibt den aktuellen Status eines laufenden Experten an.                                                       |
| [**Filter Object**](filterobject.md)                   | Definiert die Anzeige Filter Merkmale für einen Experten.                                              |
| [**Nmeventdata**](nmeventdata.md)                     | Enthält Informationen zu einer im expertenviewer angezeigten Zeile.                                      |
| [**Nmcolumninfo**](nmcolumninfo.md)                   | Stellt Informationen bereit, die eine Spalte in der Ereignisanzeige definieren.                                        |
| [**Nmcolumnvariant**](nmcolumnvariant.md)             | Stellt einen Container für alle möglichen Daten bereit, die in eine Spalte in einer Zeile in der Ereignisanzeige eingefügt werden.     |
| [**Nmcolumntype**](nmcolumntype.md)                   | Der Einstiegspunkt in der Variante, der angibt, welches Element der Union verwendet werden soll, und wie es formatiert werden soll. |



 

Netzwerkmonitor bietet auch Exportfunktionen (Hilfsfunktionen, die der Experte aufgerufen werden kann) und Enumerationen.



| Informationen über                                          | Finden Sie unter                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Exportieren Sie Funktionen, die Einstiegspunkte für Ihre expertendll bereitstellen. | [Export Funktionen der Experten-dll](expert-dll-export-functions.md)               |
| Hilfsfunktionen, die von Experten und Parser aufgerufen werden können.    | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |
| Hilfsfunktionen, die nur von Experten aufgerufen werden.              | [Expertenfunktionen](expert-functions.md)                                     |
| Enumerationen, die von expertenstrukturen und-Funktionen verwendet werden.          | [Expertenenumerationen](expert-enumerations.md)                               |



 

 

 



