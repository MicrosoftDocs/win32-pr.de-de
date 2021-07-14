---
title: FontControl-Beispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die zum Implementieren eines FontControl-Ausdrucks innerhalb einer Windows Ribbon-Anwendung erforderlich sind.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 52a81a1a1950305437a7bbc68aab95876b3a6374
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691759"
---
# <a name="fontcontrol-sample"></a>FontControl-Beispiel

Dieses Codebeispiel veranschaulicht das Markup und den Code, die zum Implementieren eines FontControl-Ausdrucks innerhalb einer Windows Ribbon-Anwendung erforderlich sind.

- [Verwendung](#usage)
  - [Erstellen des Beispiels](#building-the-sample)
  - [Ausführen des Beispiels](#running-the-sample)
- [Support](#support)
- [Mindestanforderungen](#minimum-requirements)
- [Zugehörige Themen](#related-topics)

## <a name="usage"></a>Usage

Die Windows Menüband-Frameworkbeispiele können als eigenständige Microsoft Visual Studio Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)installiert werden.

- Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ FontControl

### <a name="building-the-sample"></a>Erstellen des Beispiels

Laden Sie das Beispiel herunter.

Installieren Sie das Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung. Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.

Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels. Geben Sie an der Eingabeaufforderung MSBUILD ein.

Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.

### <a name="running-the-sample"></a>Ausführen des Beispiels

Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe Dateien im Ordner Bin \\ Debug oder Bin Release \\ aus, der im Beispielquellordner enthalten ist.

Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.

## <a name="support"></a>Unterstützung

Das [Windows Menübandentwicklungsforum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) ist verfügbar, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.

## <a name="minimum-requirements"></a>Mindestanforderungen



| Anforderung | Wert |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 7<br/> Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Unterstützte Mindestversion (Server) | Windows Server 2008 R2<br/> Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Header- und IDL-Dateien     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> Das [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows Menübandanwendungen auf Windows Vista und Windows Server 2008 ausrichten können. Die Plattformupdates sind über Windows Update für alle Kunden von Windows Vista und Windows Server 2008 verfügbar. Drittanbieteranwendungen, die [Plattformupdates für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche Update installiert ist. Andernfalls wird Windows Update heruntergeladen und im Hintergrund installiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





