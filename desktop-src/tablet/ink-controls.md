---
description: Übersicht über Ink-Steuerelemente für den Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Ink-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f07a26d30746f99b291053276de20ef78c5ce4b4f0c7a14afce6633684b7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032338"
---
# <a name="ink-controls"></a>Ink-Steuerelemente

Die Tablet PC-Plattform bietet zwei Steuerelemente: [InkEdit](inkedit-control.md) und [InkPicture,](inkpicture-control.md)mit denen Sie Tablet PC-Anwendungen ganz einfach Freihand- und Handschrifterkennung hinzufügen können. Das InkEdit-Steuerelement verfügt über [verwaltete](/previous-versions/ms835842(v=msdn.10)), [ActiveX-](inkedit-control-reference.md) und Win32-Versionen, während InkPicture nur über die verwalteten [InkPicture-](/previous-versions/ms583740(v=vs.100)) und [ActiveX-Versionen](inkpicture-control-reference.md) verfügt.

Der Hauptunterschied zwischen den Steuerelementen besteht darin, wie Daten gespeichert werden. Das [InkEdit-Steuerelement](inkedit-control.md) speichert Ink Als Text standardmäßig, [während InkPicture Ink](inkpicture-control.md) als Ink speichert.

Das [InkEdit-Steuerelement](inkedit-control.md) ist für die Texteingabe durch Handschrifterkennung vorgesehen. [InkPicture](inkpicture-control.md) ist für Anmerkungen vorgesehen (z. B. Markieren einer Präsentationsfolie oder eines anderen Bilds).

Erstellen Sie in verwaltetem Code Ink-Steuerelemente im gleichen Thread wie der Hauptthread für das Formular. Wenn ein [InkEdit-](inkedit-control.md) oder [InkPicture-Steuerelement](inkpicture-control.md) in einem anderen Thread erstellt wird, reagiert Ihre Anwendung möglicherweise nicht ordnungsgemäß.

Sie sollten das Threadingmodell explizit in singlethread apartment (STA) ändern, bevor Sie ein Ink-Steuerelement erstellen. Dadurch wird das Steuerelement im Hauptthread erstellt. Sie können den folgenden verwalteten C++-Code verwenden, um das Threadingmodell explizit festzulegen.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Sie können den folgenden Code verwenden, um dasselbe in C zu \# tun.


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Um einen Speicherverlust in verwaltetem Code zu vermeiden, müssen Sie explizit die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) für jedes Tablet PC-Steuerelement aufrufen, an das ein Ereignishandler angefügt wurde, bevor das Steuerelement den Gültigkeitsbereich übergibt.

In den folgenden Abschnitten werden Freihandsteuerelemente und die Verwendung von Freihandsteuerelementen in Anwendungen beschrieben:

-   [Hinzufügen von Ink-Steuerelementen zu einem Project](adding-ink-controls-to-a-project.md)
-   [InkEdit-Steuerelement](inkedit-control.md)
-   [InkPicture-Steuerelement](inkpicture-control.md)

 

 
