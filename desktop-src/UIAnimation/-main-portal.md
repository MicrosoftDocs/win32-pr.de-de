---
title: Windows Animations-Manager
description: Der Windows Animation Manager (Windows Animation) ermöglicht eine umfassende Animation von Benutzeroberflächenelementen.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows Animation Windows Animation , Portal
- Windows Animation Manager Windows Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e6a8f81fbef55525eff04df52a31f8ee942707c354697658ee0ba01647d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755614"
---
# <a name="windows-animation-manager"></a>Windows Animations-Manager

## <a name="purpose"></a>Zweck

Der Windows Animation Manager (Windows Animation) ermöglicht eine umfassende Animation von Benutzeroberflächenelementen. Es wurde entwickelt, um das Hinzufügen von Animationen zur Benutzeroberfläche einer Anwendung zu vereinfachen und Entwicklern die Implementierung von Animationen zu ermöglichen, die reibungslos, natürlich und interaktiv sind.

Das Animationsframework verwaltet die Planung und Ausführung von Animationen. Es stellt eine Bibliothek nützlicher mathematischer Funktionen zum Angeben des Verhaltens eines Benutzeroberflächenelements im Laufe der Zeit zur Verfügung und ermöglicht Entwicklern auch die Implementierung benutzerdefinierter Funktionen, die zusätzliches Verhalten bereitstellen.

Windows Die Animation führt das Rendering nicht durch. sie kann mit jeder Grafikplattform verwendet werden, einschließlich Direct2D, Direct3D oder GDI+.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | Beschreibung                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Entwicklungshandbuch für Animationen](windows-animation-developer-guide.md)<br/> | Das Entwicklerhandbuch bietet eine Übersicht über Windows Animation und enthält Beispielcode, der die grundlegenden Animationsaufgaben behandelt.<br/>          |
| [Windows Animationsreferenz](windows-animation-reference.md)<br/>               | Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für den Windows Animation Manager.<br/>                           |
| [Windows Animationsbeispiele](windows-animation-samples.md)<br/>                   | Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation Windows Animation Manager unterstützen. <br/> |
| [Windows Animationsglossar](-ui-animation-glossary.md)<br/>                     | Dieses Glossar enthält Begriffe und Akronyme, die für Entwickler von Interesse sind, die den Windows Animation Manager verwenden.<br/>                               |



 

## <a name="developer-audience"></a>Entwicklergruppe

Windows Animation ist für die Verwendung durch erfahrene C/C++-Entwickler konzipiert, die mit COM, Ui-Programmierkonzepten und allgemeinen Animationskonzepten vertraut sind.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Der Windows Animation Manager wurde in Windows 7 eingeführt.

Anwendungen, die Unterstützung für Windows Animation Manager unter Windows Vista erfordern, können das Plattformupdate für Windows Vista nutzen. Anwendungen, für die ein Plattformupdate für Windows Vista erforderlich ist, können Windows Update sicherstellen, dass es installiert ist, oder es im Hintergrund herunterladen und andernfalls installieren. Weitere Informationen finden Sie unter [Informationen zum Plattformupdate für Windows Vista.](../win7ip/platform-update-for-windows-vista-overview.md)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

-   [Windows Übersicht über Animationen von Animationen](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (Video)
-   [Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (Video)
-   [Windows Animation – Erweiterte Themen](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (Video)
-   [Windows Beispielcode für den Animations-Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über Animationen (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)