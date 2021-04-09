---
description: Entwickler können die WMI-Infrastruktur durch die Entwicklung von WMI-Anbietern erweitern.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Erstellen von WMI-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050593"
---
# <a name="creating-wmi-providers"></a>Erstellen von WMI-Anbietern

Entwickler können die WMI-Infrastruktur durch die Entwicklung von WMI-Anbietern erweitern. WMI-Anbieter sind COM-Objekte, die einen angegebenen Satz von Schnittstellen implementieren und bis vor kurzem in C++ immer implementiert wurden. Sie können jetzt verwaltete Sprachen wie c# verwenden, um WMI-Anbieter zu implementieren. In Version 3,5 von .NET Framework wurde das Framework für WMI-Anbieter Erweiterungen eingeführt, das Dies ermöglicht. Weitere Informationen zum Erstellen von WMI-Anbietern mithilfe dieses Frameworks finden Sie im Artikel [Schreiben von gekoppelten WMI-Anbietern mithilfe der WMI.NET-Anbieter Erweiterung 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> Sie können auch einen Anbieter mithilfe der Windows-Verwaltungsinfrastruktur (Mi) erstellen, der WMI-Version der nächsten Generation. Weitere Informationen finden Sie unter [Implementieren eines Mi-Anbieters](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

In der folgenden Tabelle werden die Inhalte dieses Abschnitts beschrieben.



| Thema                                                      | BESCHREIBUNG                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Bereitstellen von Daten für WMI](providing-data-to-wmi.md)         | Bietet einen Überblick über die Schritte zum Erstellen eines WMI-Anbieters.         |
| [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md) | Beschreibt Aufgaben, die Sie beim Erstellen verschiedener Typen von WMI-Anbietern ausführen müssen. |



 

 

 
