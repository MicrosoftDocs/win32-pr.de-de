---
title: FontControl-Beispiel
description: In diesem Codebeispiel werden das Markup und der Code veranschaulicht, die zum Implementieren eines FontControl-Objekts in einer Windows-Anwendung erforderlich sind.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 99e7ad587820ac18ce83d673efaa972f0f3b75c4547ddc7e8b4889a0e17e3bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202173"
---
# <a name="fontcontrol-sample"></a>FontControl-Beispiel

In diesem Codebeispiel werden das Markup und der Code veranschaulicht, die zum Implementieren eines FontControl-Objekts in einer Windows-Anwendung erforderlich sind.

- [Verwendung](#usage)
  - [Erstellen des Beispiels](#building-the-sample)
  - [Ausführen des Beispiels](#running-the-sample)
- [Unterstützung](#support)
- [Mindestanforderungen](#minimum-requirements)
- [Zugehörige Themen](#related-topics)

## <a name="usage"></a>Verbrauch

Die Windows Ribbon Framework-Beispiele können als eigenständige Microsoft Visual Studio-Projekte aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) heruntergeladen oder als Teil des Windows Software Development Kit [(SDK) installiert werden.](https://developer.microsoft.com/windows/downloads/sdk-archive/)

- Windows Software Development Kit (SDK) (Standardinstallationspfad): %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Beispiele \\ winui \\ WindowsRibbon \\ FontControl

### <a name="building-the-sample"></a>Erstellen des Beispiels

Laden Sie das Beispiel herunter.

Installieren Sie Windows SDK für Windows 7, und öffnen Sie das Befehlsfenster der Buildumgebung. Zeigen Sie im Startmenü auf Alle Programme und Microsoft Windows SDK, und klicken Sie dann auf CMD Shell.

Um das Beispiel über das Buildumgebungs-Befehlsfenster zu erstellen, wechseln Sie zum Quellverzeichnis des Beispiels. Geben Sie an der Eingabeaufforderung MSBUILD ein.

Um das Beispiel mit in Microsoft Visual Studio zu erstellen, laden Sie die Projektmappe oder Projektdatei des Beispiels, und drücken Sie STRG+UMSCHALT+B.

### <a name="running-the-sample"></a>Ausführen des Beispiels

Um das Beispiel über das Befehlsfenster der Buildumgebung auszuführen, führen Sie die .exe-Dateien im Ordner Bin Debug oder Bin Release aus, der \\ im Beispielquellenordner \\ enthalten ist.

Um das kompilierte Beispiel in Visual Studio mit Debuggen auszuführen, drücken Sie F5.

## <a name="support"></a>Support

Das [Windows Forum für die Menübandentwicklung](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) ist verfügbar, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung Windows Menübandanwendungen zu stellen.

## <a name="minimum-requirements"></a>Mindestanforderungen



| Anforderung | Wert |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 7<br/> Windows Vista mit Service Pack 2 (SP2) und [Plattformupdate für Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Unterstützte Mindestversion (Server) | Windows Server 2008 R2<br/> Windows Server 2008 mit SP2 und [Plattformupdate für Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Header- und IDL-Dateien     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> Das [Plattformupdate](https://msdn.microsoft.com/library/dd378748.aspx) für Windows Vista und das Plattformupdate für [Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sind Sätze von Laufzeitbibliotheken, mit denen Entwickler Windows-Menübandanwendungen sowohl auf Windows Vista als auch auf Windows Server 2008 als Ziel verwenden können. Die Plattformupdates sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows verfügbar. Bei Anwendungen von Drittanbietern, für die ein Plattformupdate für [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) oder ein Plattformupdate für Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) erforderlich ist, kann Windows Update erkennen, ob die erforderliche Aktualisierung installiert ist. Ist dies nicht der Windows Update wird es heruntergeladen und im Hintergrund installiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





