---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Teilmenge von .NET 2,0 jetzt auf Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218823"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Teilmenge von .NET 2,0 jetzt auf Server Core

## <a name="platform"></a>Plattform

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Die Server Core-Installationsoption für Windows Server 2008 R2 enthält jetzt eine Teilmenge der .NET Framework 2,0. Die Teilmenge ist die Funktionalität in .NET 2,0, die mit der Funktionalität in Server Core abgestimmt ist. der Server Core-Basis wurden keine Binärdateien hinzugefügt, um die Funktionsweise eines beliebigen Teils von .NET 2,0 zu ermöglichen.

In der Server Core-Installationsoption für Windows Server 2008 wurde keine .NET-Unterstützung unterstützt.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Dadurch können einige auf .NET 2,0 basierende Anwendungen auf Server Core in Windows Server 2008 R2 ausgeführt werden.

## <a name="testing"></a>Test

Vergewissern Sie sich, dass die .NET-Klassen, die Ihr Code verwendet, in Server Core enthalten sind Testen Sie außerdem alle Anwendungen, die diesen Code auf Server Core ausführen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Server Core-Blog](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Weitere Informationen finden Sie auch* im Abschnitt Server Core des *Windows Server 2008 R2 SDK* , sobald es verfügbar ist.

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.

 

 

 
