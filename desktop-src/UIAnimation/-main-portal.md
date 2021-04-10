---
title: Windows-Animations-Manager
description: Der Windows Animation Manager (Windows-Animation) ermöglicht eine umfangreiche Animation von Benutzeroberflächen Elementen.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows Animation Windows Animation, Portal
- Windows Animation Manager-Windows-Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948863"
---
# <a name="windows-animation-manager"></a>Windows-Animations-Manager

## <a name="purpose"></a>Zweck

Der Windows Animation Manager (Windows-Animation) ermöglicht eine umfangreiche Animation von Benutzeroberflächen Elementen. Es wurde entwickelt, um den Prozess des Hinzufügens von Animationen zur Benutzeroberfläche einer Anwendung zu vereinfachen und Entwicklern das Implementieren von Animationen zu ermöglichen, die nahtlos, natürlich und interaktiv sind.

Das Animations Framework verwaltet die Planung und die Ausführung von Animationen. Es stellt eine Bibliothek nützlicher mathematischer Funktionen zum Angeben des Verhaltens eines Benutzeroberflächen Elements im Zeitverlauf bereit und ermöglicht es Entwicklern außerdem, benutzerdefinierte Funktionen zu implementieren, die zusätzliche Verhaltensweisen bereitstellen.

Das Rendering wird von der Windows-Animation nicht durchgeführt. Sie kann mit jeder beliebigen Grafik Plattform verwendet werden, einschließlich Direct2D, Direct3D oder GDI+.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Entwicklungs Leit Faden für Windows-Animationen](windows-animation-developer-guide.md)<br/> | Im Entwicklerhandbuch finden Sie eine Übersicht über die Windows-Animation und einen Beispielcode, der die grundlegenden Animations Aufgaben behandelt.<br/>          |
| [Referenz zur Windows-Animation](windows-animation-reference.md)<br/>               | Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für den Windows-Animations-Manager.<br/>                           |
| [Beispiele für Windows-Animationen](windows-animation-samples.md)<br/>                   | Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation zu Windows Animation Manager unterstützen. <br/> |
| [Glossar für Windows-Animationen](-ui-animation-glossary.md)<br/>                     | Dieses Glossar enthält Begriffe und acronyme, die für Entwickler interessant sind, die den Windows-Animations-Manager verwenden.<br/>                               |



 

## <a name="developer-audience"></a>Entwicklergruppe

Die Windows-Animation ist für die Verwendung durch erfahrene C/C++-Entwickler konzipiert, die mit com, Programmier Konzepten für die Benutzeroberfläche und allgemeinen Animations Konzepten vertraut sind.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Der Windows Animation Manager wurde in Windows 7 eingeführt.

Anwendungen, die Unterstützung für Windows Animation Manager unter Windows Vista benötigen, können das Platt Form Update für Windows Vista nutzen. Anwendungen, für die ein Platt Form Update für Windows Vista erforderlich ist, können Windows Update überprüfen, ob es installiert ist, oder Sie können es im Hintergrund herunterladen und installieren. Weitere Informationen finden Sie unter Informationen zum [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

-   [Übersicht über Windows Scenic Animation](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (Video)
-   [In Windows 7: Deep Dive und Tutorial zu Animation Manager](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (Video)
-   [Windows-Animation-erweiterte Themen](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (Video)
-   [Windows Animation Manager-Beispiel Code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über Animationen (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)