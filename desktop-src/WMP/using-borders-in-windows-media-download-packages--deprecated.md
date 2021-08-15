---
title: Verwenden von Rahmen in Windows Mediendownloadpaketen (veraltet)
description: Verwenden von Rahmen in Windows Mediendownloadpaketen (veraltet)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows Medienmetadateien Windows Mediendownloadpakete
- Windows Media Player,Windows Mediendownloadpakete
- Metafiles,Windows Mediendownloadpakete
- Windows Medien,Windows Mediendownloadpakete
- Rahmen,about
- Windows Mediendownloadpakete,Rahmen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 851edf0d2291d41212cf44829219235426463733ce95a99c3d59187eba490ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931808"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Verwenden von Rahmen in Windows Mediendownloadpaketen (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von Windows Media Player und des Windows Media Player SDK möglicherweise nicht verfügbar ist.

Mit Rahmen können Sie eine benutzerdefinierte grafische Benutzeroberfläche für Ihre gepackten Inhalte erstellen. Der Rahmen kann Elemente wie Bilder, interaktive Steuerelemente und Links zu Websites enthalten. Sie können Rahmen in Fällen verwenden, in denen Sie Ihren gepackten Inhalten einen zusätzlichen Wert hinzufügen möchten, z. B. für Branding oder Werbung. Nachdem Benutzer Ihr Downloadpaket für Windows Medien heruntergeladen und geöffnet haben, zeigt Windows Media Player automatisch Ihren benutzerdefinierten Rahmen an, wenn der gepackte Inhalt wiedergeknüht wird.

Im Gegensatz zu einer Skin, die es Benutzern ermöglicht, die Windows Media Player-Benutzeroberfläche  vollständig zu ersetzen, wird ein Rahmen nur im Bereich Jetzt wieder verwendet des Vollmodusplayers angezeigt. Die gleichen Tools und Technologien, die Sie zum Erstellen von Skins verwenden, werden jedoch auch zum Erstellen von Rahmen verwendet. Die folgende Abbildung zeigt einen Rahmen.

![Ein Rahmen, der inwindows Media Player 10 angezeigt wird](images/border-v10.png)

Es ist wichtig, die grundlegenden Techniken zum Erstellen einer Skin zu verstehen, bevor Sie versuchen, einen Rahmen zu erstellen. Die Border-Programmierung erfolgt mithilfe von zwei Programmiersprachen: Extensible Markup Language (XML) und Microsoft JScript. XML wird verwendet, um Schnittstellenelemente wie Schaltflächen, Schieberegler und Textfelder zu definieren. Sie müssen nicht alle Xml-Details verstehen, da Sie keine neuen XML-Codeelemente schreiben müssen. Sie können einfach diejenigen verwenden, die von Windows Media Player. Obwohl JScript zum Erstellen von Rahmen nicht erforderlich ist, können sie verwendet werden, um zusätzliche Funktionen zur Verfügung zu stellen.

Eine komprimierte Rahmendatei mit der Dateinamenerweiterung WMZ enthält eine Rahmendefinitionsdatei mit der Dateierweiterung WMS und alle image-Dateien, die innerhalb des Rahmens verwendet werden.

Um einen Rahmen in ein Mediendownloadpaket Windows, erstellen Sie einfach einen Rahmen und einen Verweis auf diesen Rahmen in einer Wiedergabeliste Windows Medienmetadatei. Die Rahmendatei wird in Windows Media Player, nachdem der Player die Metadatei analysiert und das **SKIN-Element** interpretiert, das auf den Rahmen verweist. Das **SKIN-Element** wird nur für Rahmen verwendet, und das HREF-Attribut des **SKIN-Elements** kann für jedes Paket nur auf eine Skin verweisen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Rahmen für Windows Media Player (veraltet)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Mediendownloadpakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media Player Skins**](windows-media-player-skins.md)
</dt> </dl>

 

 




