---
title: Auswählen von Dateien
description: Auswählen von Dateien
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- Erstellen von Skins, auswählen von Dateien
- Windows Media Player Skins, auswählen von Dateien
- Skins, auswählen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207205"
---
# <a name="choosing-files"></a>Auswählen von Dateien

Wenn Sie eine Datei auswählen möchten, können Sie Code verwenden, der dem Beispiel für die Wiedergabeliste ähnelt, aber Folgendes für den Abschnitt "playelement" ersetzen:


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



In dieser Zeile wird die **OpenDialog** -Methode von **Theme** verwendet, um eine **URL** für den Player zu definieren. Sie können dies verwenden, um Dateien auszuwählen, die nicht in Wiedergabelisten vorliegen.

Ein ähnliches Funktions **offenes OpenDialog** -Beispiel finden Sie im Beispiel Abschnitt des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Erstellen von Skin**](skin-creation-guide.md)
</dt> </dl>

 

 




