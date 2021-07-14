---
title: Windows Menübandframework
description: Lesen Sie eine Einführung in das Windows-Menübandframework, das eine moderne Alternative zu den mehrschichtigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows ist.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows Bändchen
- Menüband
- Windows Menübanddokumentation
- Menübanddokumentation
- Windows Menüband-API
- Menüband-API
- Windows Menüband, Framework
- Menüband, Framework
- Windows Menüband, Informationen
- Menüband, Informationen
- Windows Menüband, Komponenten
- Menüband, Komponenten
- Windows Menüband, Ansichten
- Menüband, Ansichten
- Windows Menüband, Architektur
- Menüband, Architektur
- Windows Menüband, APIs
- Menüband, APIs
- Windows Menüband, Sicherheit
- Menüband, Sicherheit
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 98f7dbf42d604f93c76bb9897aa25918d45d126f
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691649"
---
# <a name="windows-ribbon-framework"></a>Windows Menübandframework

Das Windows-Menübandframework ist ein umfangreiches Befehlspräsentationssystem, das eine moderne Alternative zu den mehrschichtigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows bietet. Ähnlich wie bei der Funktionalität und Darstellung der Microsoft Office 2007 Fluent-Benutzeroberfläche besteht das Menübandframework aus einer Menübandbefehlsleiste, die die hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Ende eines Anwendungsfensters und ein Kontextmenüsystem verfügbar macht.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | Beschreibung                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersichten über das Menübandframework](windowsribbon-overviews-entry.md)<br/>      | In den Themen in diesem Abschnitt werden die Grundlagen des Menübandframework erläutert. <br/>                                                                                                                   |
| [Entwicklerhandbücher für Menübandframework](windowsribbon-guides-entry.md)<br/>  | In den Themen in diesem Abschnitt werden bestimmte Aspekte des Frameworks Windows Menüband beschrieben. <br/>                                                                                                          |
| [Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)<br/> | In den Themen in diesem Abschnitt werden die Steuerelemente beschrieben, die im Menübandframework enthalten sind. Die hier aufgeführten Steuerelemente sind die Benutzeroberflächenobjekte in einem Menüband, die Befehlsfunktionen verfügbar machen.<br/> |
| [Referenz zum Menübandframework](windowsribbon-reference-entry.md)<br/>      | Die in diesem Abschnitt enthaltenen Themen enthalten die Referenzspezifikationen für das Menübandframework.<br/>                                                                                                       |
| [Beispiele für Menübandframework](windowsribbon-samples-entry.md)<br/>          | Die Themen in diesem Abschnitt enthalten Details zu den Codebeispielen, die die Dokumentation Windows Menübandframework unterstützen. <br/>                                                                     |
| [Glossar zum Menübandframework](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Entwicklerzielgruppe

Das Windows-Menübandframework ist für die Verwendung durch C/C++-Entwickler und Benutzeroberflächen-Designer konzipiert.

Empfohlene Ineffizienzen:

- COM-Programmierung
- Windows API-Programmierung
- XML/XAML-Programmierung

Empfohlene grundlegende Kenntnisse:

- Konzepte der Benutzeroberflächenprogrammierung
- Allgemeine Konzepte der Benutzeroberfläche

## <a name="minimum-requirements"></a>Mindestanforderungen



| Anforderung | Wert |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)               | Windows 7<br/> Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Unterstützte Mindestversion (Server)               | Windows Server 2008 R2<br/> Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| Header- und IDL-Dateien                   | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> Das [Plattformupdate](https://msdn.microsoft.com/library/dd378748.aspx) für Windows Vista und das Plattformupdate für [Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 als Ziel verwenden können. Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows verfügbar. Bei Anwendungen von Drittanbietern, für die ein Plattformupdate für [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein Plattformupdate für Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erforderlich ist, kann Windows Update erkennen, ob das erforderliche Update installiert ist. Ist dies nicht der Windows Update wird es heruntergeladen und im Hintergrund installiert.

 

## <a name="see-also"></a>Weitere Informationen

[Component Object Model (COM)](../com/component-object-model--com--portal.md)


[Windows-API](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

