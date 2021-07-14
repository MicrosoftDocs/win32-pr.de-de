---
title: ContextPopup-Beispiel
description: In diesem Codebeispiel werden das Markup und der Code veranschaulicht, die zum Implementieren einer Windows Ribbon-Anwendung mit ContextPopups erforderlich sind.
ms.assetid: f334dbfc-710a-4652-b914-a668ae36aecd
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 5f469ac892f063fbd6c8beb0fe8af0c054216dbc
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691699"
---
# <a name="contextpopup-sample"></a>ContextPopup-Beispiel

In diesem Codebeispiel werden das Markup und der Code veranschaulicht, die zum Implementieren einer Windows Ribbon-Anwendung mit ContextPopups erforderlich sind.

- [Verwendung](#usage)
  - [Erstellen des Beispiels](#building-the-sample)
  - [Ausführen des Beispiels](#running-the-sample)
- [Support](#support)
- [Mindestanforderungen](#minimum-requirements)
- [Zugehörige Themen](#related-topics)

## <a name="usage"></a>Usage

Die Windows Ribbon Framework-Beispiele können als eigenständige Microsoft Visual Studio-Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK) installiert werden.](https://developer.microsoft.com/windows/downloads/sdk-archive/)

- Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ ContextPopup

### <a name="building-the-sample"></a>Erstellen des Beispiels

Laden Sie das Beispiel herunter.

Installieren Sie Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung. Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.

Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels. Geben Sie an der Eingabeaufforderung MSBUILD ein.

Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.

### <a name="running-the-sample"></a>Ausführen des Beispiels

Um das Beispiel über das Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe-Dateien im Ordner Bin Debug oder Bin Release aus, der \\ im Beispielquellenordner \\ enthalten ist.

Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.

## <a name="support"></a>Unterstützung

Das [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Verfügung, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.

## <a name="minimum-requirements"></a>Mindestanforderungen



| Anforderung | Wert |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 7<br/> Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Unterstützte Mindestversion (Server) | Windows Server 2008 R2<br/> Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Header- und IDL-Dateien     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> Das [Plattformupdate](https://msdn.microsoft.com/library/dd378748.aspx) für Windows Vista und das Plattformupdate für [Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 als Ziel verwenden können. Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows verfügbar. Bei Anwendungen von Drittanbietern, für die ein Plattformupdate für [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein Plattformupdate für Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erforderlich ist, kann Windows Update erkennen, ob das erforderliche Update installiert ist. Ist dies nicht der Windows Update wird es heruntergeladen und im Hintergrund installiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontext-Popup](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





