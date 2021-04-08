---
title: Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden
description: Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media-Format-SDK, Skript Befehle
- Windows Media-Format-SDK, Windows Media Player
- Advanced Systems Format (ASF), Skript Befehle
- ASF (Advanced Systems Format), Skript Befehle
- Advanced Systems Format (ASF), Windows Media Player
- ASF (Advanced Systems Format), Windows Media Player
- Skripts, Befehle
- Skripts, Windows-Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037046"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden

Das SDK für den Windows Media-Format bietet keine native Unterstützung für das Auswerten und reagieren auf Skript Befehle. Sie müssen eine beliebige Logik im Zusammenhang mit Skript Befehlen in der Anwendung einschließen. Die verwendeten Skript Typen müssen auch in der Anwendung definiert werden.

Sie können Code einschließen, um dieselben Skript Befehle zu verarbeiten, die von Windows Media Player unterstützt werden. Die Beibehaltung der Kompatibilität mit Windows-Media Player macht Ihre Dateien universeller, als wenn Sie benutzerdefinierte Skript Befehle einbetten.

In der folgenden Tabelle sind die Skript Typen aufgeführt, die von Windows Media Player unterstützt werden.



| Skripttyp | BESCHREIBUNG                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | Der Player sendet die angegebene URL an den Browser, damit Sie dem Benutzer angezeigt wird. Wenn ein eingebettetes Player-Steuerelement verwendet wird, können Sie einen bestimmten Frame Verweis auf die URL hinzufügen, indem Sie die &&*frameName* -Syntax verwenden.                                                                             |
| Einfügen    | Eine URL zu einer anderen zu Wiedergabe enden Mediendatei.                                                                                                                                                                                                                                                |
| CAPTION     | Eine Text Zeichenfolge, die im Beschriftungen Bereich von Windows Media Player angezeigt wird. Dieser Typ unterstützt die HTML-Standard Formatierung, sodass der Text so formatiert werden kann, wie Sie möchten. Ein Beispiel für die Verwendung von Untertiteln.                                                                             |
| EREIGNIS       | Der Name eines Ereignisses, das auftreten soll. Der Ereignistyp unterstützt Anpassungen für Ihre eigenen Verwendungszwecke. Der Code für das angegebene Ereignis muss in der Windows Media-Metadatendatei für den Datenstrom definiert werden, damit der Player das angegebene Ereignis ausführen muss. Ein Beispiel für die Verwendung von Werbe Einfügungs. |
| OpenEvent   | Dieses Skript befindet sich vor dem eigentlichen-Ereignis. Das OpenEvent ermöglicht dem Player, den Inhalt vorab zu puffern, damit der Wechsel zwischen Streams bei Auftreten des Ereignisses nahtlos erscheint.                                                                                                       |
| TEXT        | Eine Text Zeichenfolge, die im Beschriftungen Bereich von Windows Media Player angezeigt wird. Kann nur-Text-, Sami-oder HTML-formatierter Text sein.                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Skript Befehlen**](using-script-commands.md)
</dt> </dl>

 

 




