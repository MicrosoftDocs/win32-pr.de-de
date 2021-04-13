---
description: Übersicht über frei Hand Steuerelemente für den Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Ink-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525967"
---
# <a name="ink-controls"></a>Ink-Steuerelemente

Die Tablet PC-Plattform bietet zwei Steuerelemente: [InkEdit](inkedit-control.md) und [InkPicture](inkpicture-control.md), mit denen Sie Tablet PC-Anwendungen problemlos Handschrift und Handschrifterkennung hinzufügen können. Das InkEdit-Steuerelement verfügt über [verwaltete](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) -und Win32-Versionen, während InkPicture nur über die verwalteten [InkPicture](/previous-versions/ms583740(v=vs.100)) -und [ActiveX](inkpicture-control-reference.md) -Versionen verfügt.

Der Hauptunterschied zwischen den Steuerelementen besteht darin, wie Daten gespeichert werden. Das [InkEdit](inkedit-control.md) -Steuerelement speichert Frei Hand Eingaben standardmäßig als Text, während [InkPicture](inkpicture-control.md) Freihand als frei Hand Daten speichert.

Das [InkEdit](inkedit-control.md) -Steuerelement ist für die Texteingabe durch Handschrifterkennung vorgesehen. [InkPicture](inkpicture-control.md) ist für die Anmerkung gedacht (z. b. das Markieren einer Präsentations Folie oder eines anderen Bilds).

Erstellen Sie in verwaltetem Code frei Hand Steuerelemente im gleichen Thread wie der Haupt Thread für das Formular. Wenn ein [InkEdit](inkedit-control.md) -oder [InkPicture](inkpicture-control.md) -Steuerelement in einem anderen Thread erstellt wird, reagiert die Anwendung möglicherweise nicht ordnungsgemäß.

Sie sollten das Threading Modell explizit in ein Single Thread-Apartment (STA) ändern, bevor Sie ein Ink-Steuerelement erstellen. Dies bewirkt, dass das Steuerelement im Haupt Thread erstellt wird. Sie können den folgenden verwalteten C++-Code verwenden, um das Threading Modell explizit festzulegen.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Sie können den folgenden Code verwenden, um in C dasselbe zu tun \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Um einen Speicher Verluste zu vermeiden, müssen Sie in verwaltetem Code die verwerfen [-Methode explizit](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) für jedes Tablet PC-Steuerelement, an das ein Ereignishandler angefügt wurde, aufgerufen werden, bevor das Steuerelement den Gültigkeitsbereich verlässt.

In den folgenden Abschnitten werden Freihand Steuerelemente und die Verwendung von frei Hand Steuerelementen in-Anwendungen beschrieben:

-   [Hinzufügen von Ink-Steuerelementen zu einem Projekt](adding-ink-controls-to-a-project.md)
-   [InkEdit-Steuerelement](inkedit-control.md)
-   [InkPicture-Steuerelement](inkpicture-control.md)

 

 
