---
title: Windows-Menübandframework
description: Lesen Sie eine Einführung in das Windows-Menübandframework, das eine moderne Alternative zu den mehrstufigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen darstellt.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows-Menüband
- Menüband
- Windows-Menübanddokumentation
- Menübanddokumentation
- Windows-Menüband-API
- Menüband-API
- Windows-Menüband, Framework
- Menüband, Framework
- Windows-Menüband, Informationen
- Menüband, Informationen
- Windows-Menüband, Komponenten
- Menüband, Komponenten
- Windows-Menüband, Ansichten
- Menüband, Ansichten
- Windows-Menüband, Architektur
- Menüband, Architektur
- Windows-Menüband, APIs
- Menüband, APIs
- Windows-Menüband, Sicherheit
- Menüband, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211e1e1cf39a547ad0edbc0c180c62e2f40e15fa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406363"
---
# <a name="windows-ribbon-framework"></a>Windows-Menübandframework

Das Windows-Menübandframework ist ein umfangreiches Befehlspräsentationssystem, das eine moderne Alternative zu den mehrstufigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet. Ähnlich wie die Funktionalität und Darstellung der Microsoft Office 2007 Fluent-Benutzeroberfläche besteht das Menübandframework aus einer Menübandbefehlsleiste, die die Hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Rand eines Anwendungsfensters und ein Kontextmenüsystem verfügbar macht.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | Beschreibung                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersichten über Menübandframeworks](windowsribbon-overviews-entry.md)<br/>      | In den Themen in diesem Abschnitt werden die Grundlagen des Menübandframeworks erläutert. <br/>                                                                                                                   |
| [Entwicklerhandbücher für Menübandframeworks](windowsribbon-guides-entry.md)<br/>  | In den Themen in diesem Abschnitt werden bestimmte Aspekte des Windows-Menübandframeworks beschrieben. <br/>                                                                                                          |
| [Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)<br/> | In den Themen in diesem Abschnitt wird der Satz von Steuerelementen beschrieben, die im Menübandframework enthalten sind. Die hier aufgeführten Steuerelemente sind die Benutzeroberflächenobjekte in einem Menüband, die die Befehlsfunktionalität verfügbar machen.<br/> |
| [Referenz zum Menübandframework](windowsribbon-reference-entry.md)<br/>      | Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für das Menübandframework.<br/>                                                                                                       |
| [Menüband-Frameworkbeispiele](windowsribbon-samples-entry.md)<br/>          | Die in diesem Abschnitt enthaltenen Themen enthalten Details zu den Codebeispielen, die die Windows Ribbon Framework-Dokumentation unterstützen. <br/>                                                                     |
| [Menübandframeworkglossar](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Entwicklerzielgruppe

Das Windows-Menübandframework ist für die Verwendung durch C/C++-Entwickler und Benutzeroberflächen-Designer konzipiert.

Empfohlene Obszönen:

-   COM-Programmierung
-   Windows-API-Programmierung
-   XML-/XAML-Programmierung

Empfohlene grundlegende Kenntnisse:

-   Konzepte der Benutzeroberflächenprogrammierung
-   Allgemeine Konzepte der Benutzeroberfläche

## <a name="minimum-requirements"></a>Mindestanforderungen



| Anforderung | Wert |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)               | Windows 7<br/> Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Unterstützte Mindestversion (Server)               | Windows Server 2008 R2<br/> Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| Header- und IDL-Dateien                   | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> Platform [Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und Platform Update für Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen auf Windows Vista und Windows Server 2008 ausrichten können. Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows Update verfügbar. Drittanbieteranwendungen, die [Platform Update für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder Platform Update für Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche update installiert ist. Andernfalls werden Windows Update sie herunterladen und im Hintergrund installieren.

 

## <a name="see-also"></a>Weitere Informationen

[Component Object Model (COM)](../com/component-object-model--com--portal.md)


[Windows-API](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

