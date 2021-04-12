---
title: Verwenden von Rahmen in Windows-Medien Download Paketen (veraltet)
description: Verwenden von Rahmen in Windows-Medien Download Paketen (veraltet)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Rahmen, Informationen
- Windows Media Download Packages, Rahmen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388398"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Verwenden von Rahmen in Windows-Medien Download Paketen (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Rahmen ermöglichen es Ihnen, eine angepasste grafische Benutzeroberfläche für Ihren verpackten Inhalt zu erstellen. Der Rahmen kann Elemente enthalten, wie z. b. Bilder, interaktive Steuerelemente und Links zu Websites. Sie können Rahmen in Fällen verwenden, in denen Sie Ihren gepackten Inhalt, z. b. Branding oder Werbung, zusätzlichen Wert hinzufügen möchten. Nachdem Benutzer Ihr Windows Media-Downloadpaket heruntergeladen und geöffnet haben, zeigt Windows Media Player automatisch Ihren benutzerdefinierten Rahmen an, wenn der gepackte Inhalt wiedergegeben wird.

Im Gegensatz zu einem Skin, das es Benutzern ermöglicht, die Benutzeroberfläche von Windows Media Player vollständig zu ersetzen, wird ein Rahmen nur im Fenster " **jetzt** wiedergegeben" des vollmodusplayers angezeigt. Die gleichen Tools und Technologien, die Sie zum Erstellen von Skins verwenden, werden jedoch auch zum Erstellen von Rahmen verwendet. Die folgende Abbildung zeigt einen Rahmen.

![ein Rahmen, der in Windows Media Player 10 angezeigt wird.](images/border-v10.png)

Es ist wichtig, sich mit den grundlegenden Techniken zum Erstellen einer Skin vertraut zu machen, bevor Sie versuchen, einen Rahmen zu erstellen. Die Rahmen Programmierung erfolgt mithilfe von zwei Programmiersprachen: Extensible Markup Language (XML) und Microsoft JScript. XML wird zum Definieren von Schnittstellen Elementen verwendet, z. b. Schaltflächen, Schieberegler und Textfelder. Sie müssen nicht alle XML-Details verstehen, da Sie keine neuen XML-Code Elemente schreiben müssen. Sie können einfach die von Windows Media Player bereitgestellten verwenden. Obwohl JScript zum Erstellen von Rahmen nicht erforderlich ist, kann es verwendet werden, um zusätzliche Funktionalität bereitzustellen.

Eine komprimierte Rahmen Datei mit der Dateinamenerweiterung. WMZ enthält eine Rahmen Definitionsdatei mit der Dateinamenerweiterung. WMS und alle Bilddateien, die innerhalb des Rahmens verwendet werden.

Wenn Sie einen Rahmen in ein Windows Media Download-Paket einschließen möchten, erstellen Sie einfach einen Rahmen, und verweisen Sie auf diesen Rahmen in einer Windows Media Metadatei-Wiedergabeliste. Die Rahmen Datei wird in Windows Media Player geladen, nachdem der Player die Metadatendatei analysiert und das **Skin** -Element interpretiert hat, das auf den Rahmen verweist. Das **Skin** -Element wird nur für Rahmen verwendet, und das href-Attribut des **Skin** -Elements kann nur auf ein Skin für jedes Paket verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Rahmen für Windows-Media Player (veraltet)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Media-Download Pakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media Player Skins**](windows-media-player-skins.md)
</dt> </dl>

 

 




