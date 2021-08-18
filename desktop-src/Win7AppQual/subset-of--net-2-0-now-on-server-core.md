---
description: Teilmenge von .NET 2.0 jetzt auf Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Teilmenge von .NET 2.0 jetzt auf Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9da259186f0eaea7999df6dde6d42d972484c35eee24c9b9efb7fc6a5d882b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994630"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Teilmenge von .NET 2.0 jetzt auf Server Core

## <a name="platform"></a>Plattform

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>BESCHREIBUNG

Die Server Core-Installationsoption für Windows Server 2008 R2 enthält jetzt eine Teilmenge der .NET Framework 2.0. Die Teilmenge ist die Funktionalität in .NET 2.0, die mit der Funktionalität in Server Core übereinstimmt. der Server Core-Basis wurden keine Binärdateien hinzugefügt, damit ein Teil von .NET 2.0 funktioniert.

Die Server Core-Installationsoption für Windows Server 2008 wurde nicht von .NET unterstützt.

## <a name="manifestation-of-impact"></a>Auswirkungen

Dadurch können einige .NET 2.0-basierte Anwendungen unter Server Core in Windows Server 2008 R2 ausgeführt werden.

## <a name="testing"></a>Testen

Vergewissern Sie sich, dass die von Ihrem Code verwendeten .NET-Klassen in Server Core enthalten sind. Testen Sie auch alle Anwendungen, die diesen Code auf Server Core ausführen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Server Core-Blog](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Weitere Informationen finden Sie auch* im Abschnitt Server Core des Windows Server *2008 R2 SDK,* sobald es verfügbar ist.

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.

 

 

 
