---
description: Entwickler können die WMI-Infrastruktur erweitern, indem sie WMI-Anbieter entwickeln.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Erstellen von WMI-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cb15b911cb549e28e3536da0a9da31de8df1d6f395ede5f9c9176d21239abc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679740"
---
# <a name="creating-wmi-providers"></a>Erstellen von WMI-Anbietern

Entwickler können die WMI-Infrastruktur erweitern, indem sie WMI-Anbieter entwickeln. WMI-Anbieter sind COM-Objekte, die einen angegebenen Satz von Schnittstellen implementieren und bis vor Kurzem immer in C++ implementiert wurden. Sie können jetzt verwaltete Sprachen wie C# verwenden, um WMI-Anbieter zu implementieren. In Version 3.5 von .NET Framework wurde das Framework für WMI-Anbietererweiterungen eingeführt, das dies ermöglicht. Weitere Informationen zum Erstellen von WMI-Anbietern mithilfe dieses Frameworks finden Sie im Artikel Schreiben gekoppelter WMI-Anbieter mit WMI.NET [Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> Sie können einen Anbieter auch mithilfe Windows Management Infrastructure (MI) erstellen, der WMI-Version der nächsten Generation. Weitere Informationen finden Sie unter [Implementieren eines MI-Anbieters.](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider)

 

In der folgenden Tabelle werden die Inhalte in diesem Abschnitt beschrieben.



| Thema                                                      | Beschreibung                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)         | Bietet eine Übersicht über die Schritte zum Erstellen eines WMI-Anbieters.         |
| [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md) | Beschreibt Aufgaben, die Sie beim Erstellen verschiedener Typen von WMI-Anbietern ausführen müssen. |



 

 

 
