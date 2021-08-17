---
title: ContextPopup-Beispiel
description: Dieses Codebeispiel veranschaulicht das Markup und den Code, die erforderlich sind, um eine Windows Menübandanwendung mit ContextPopups zu implementieren.
ms.assetid: f334dbfc-710a-4652-b914-a668ae36aecd
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: f0c739e368a26b2664b71efd4ff7cd8c3e7f8490ef7df8ccbe8ec6ace18af115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964389"
---
# <a name="contextpopup-sample"></a>ContextPopup-Beispiel

Dieses Codebeispiel veranschaulicht das Markup und den Code, die erforderlich sind, um eine Windows Menübandanwendung mit ContextPopups zu implementieren.

- [Verwendung](#usage)
  - [Erstellen des Beispiels](#building-the-sample)
  - [Ausführen des Beispiels](#running-the-sample)
- [Unterstützung](#support)
- [Mindestanforderungen](#minimum-requirements)
- [Zugehörige Themen](#related-topics)

## <a name="usage"></a>Verbrauch

Die Frameworkbeispiele für Windows Menüband können als eigenständige Microsoft Visual Studio Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)installiert werden.

- Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ ContextPopup

### <a name="building-the-sample"></a>Erstellen des Beispiels

Laden Sie das Beispiel herunter.

Installieren Sie das Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung. Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.

Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels. Geben Sie an der Eingabeaufforderung MSBUILD ein.

Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.

### <a name="running-the-sample"></a>Ausführen des Beispiels

Um das Beispiel im Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe Dateien im Ordner Bin \\ Debug oder Bin Release \\ aus, der im Beispielquellordner enthalten ist.

Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.

## <a name="support"></a>Support

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
> Das [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) und das [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows Menübandanwendungen auf Windows Vista und Windows Server 2008 ausrichten können. Die Plattformupdates sind für alle Kunden von Windows Vista und Windows Server 2008 über Windows Update verfügbar. Drittanbieteranwendungen, die [Plattformupdates für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erfordern, können Windows Update erkennen, ob das erforderliche Update installiert ist. Andernfalls wird Windows Update heruntergeladen und im Hintergrund installiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontext-Popup](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





