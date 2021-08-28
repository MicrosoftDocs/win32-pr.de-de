---
title: Verwenden von Skriptbefehlen, die von Windows Media Player
description: Verwenden von Skriptbefehlen, die von Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Medienformat-SDK, Skriptbefehle
- Windows Medienformat-SDK,Windows Media Player
- Advanced Systems Format (ASF), Skriptbefehle
- ASF (Advanced Systems Format), Skriptbefehle
- Advanced Systems Format (ASF), Windows Media Player
- ASF (Advanced Systems Format), Windows Media Player
- Skripts, Befehle
- scripts,Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58709af99cb4ebcb4eaba64fa6bb167b0ca80acb3fcb21b34efe4a55e2bacf12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110070"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Verwenden von Skriptbefehlen, die von Windows Media Player

Das Windows Media Format SDK bietet keine native Unterstützung für das Analyse- und Reagieren auf Skriptbefehle. Sie müssen eine beliebige Logik im Zusammenhang mit Skriptbefehlen in Ihre Anwendung eingeben. Die skripttypen, die Sie verwenden, müssen auch in Ihrer Anwendung definiert werden.

Sie können Code verwenden, um dieselben Skriptbefehle zu verarbeiten, die von der Windows Media Player. Durch die Aufrechterhaltung der Windows Media Player werden Ihre Dateien universeller, als wenn Sie benutzerdefinierte Skriptbefehle einbetten.

In der folgenden Tabelle sind skripttypen aufgeführt, die von der Windows Media Player.



| Skripttyp | Beschreibung                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | Der Player sendet die angegebene URL zur Anzeige für den Benutzer an den Browser. Wenn ein eingebettetes Player-Steuerelement verwendet wird, können Sie der URL einen bestimmten Frameverweis hinzufügen, indem Sie &&*Framename-Syntax* verwenden.                                                                             |
| Dateiname    | Eine URL zu einer anderen Mediendatei, die abgespielt werden soll.                                                                                                                                                                                                                                                |
| CAPTION     | Eine Textzeichenfolge, die im Beschriftungsbereich des -Windows Media Player. Dieser Typ unterstützt die HTML-Standardformatierung, sodass der Text nach Be wunsch formatiert werden kann. Ein Beispiel für die Verwendung ist die Untertitelung.                                                                             |
| EREIGNIS       | Der Name eines Ereignisses, das auftreten soll. Der EVENT-Typ unterstützt die Anpassung für Ihre eigenen Zwecke. Der Code für das angegebene Ereignis muss in der Windows Media-Metadatei für den Stream definiert werden, damit der Player das angegebene Ereignis ausführen kann. Ein Beispiel für die Verwendung ist das Einfügen von Werbeeinblendung. |
| OPENEVENT   | Dieses Skript geht dem tatsächlichen EREIGNIS voraus. OpenEVENT ermöglicht es dem Player, den Inhalt vorab zu puffern, sodass der Wechsel zwischen Streams beim Auftreten des EREIGNISSEs nahtlos erscheint.                                                                                                       |
| TEXT        | Eine TEXT-Zeichenfolge, die im Beschriftungsbereich des Windows Media Player. Kann Nur-Text, SAMI- oder HTML-formatierten Text sein.                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Skriptbefehlen**](using-script-commands.md)
</dt> </dl>

 

 




