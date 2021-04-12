---
title: Debuggen von Code
description: Debuggen von Code
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Windows Media Player Skins, Debuggen von Code
- Skins, Debuggen von Code
- Debuggen von Code für Skins
- Windows Media Player Skins, Protokollierung
- Skins, Protokollierung
- Protokollierungs Funktionalität in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311056"
---
# <a name="debugging-code"></a>Debuggen von Code

Häufig möchten Sie sehen, was in der Skin passiert. Hierfür können Sie ein Text Steuerelement oder eine Protokolldatei verwenden.

Sie können ein **Text** Element erstellen und es temporär in einem Teil der Skin platzieren. Beispielsweise können Sie den folgenden Code verwenden, um das **Text** -Element zu erstellen:


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



Wenn Sie z. b. die aktuelle Position des Inhalts digitaler Medien in Windows Media Player anzeigen möchten, können Sie Code wie den folgenden verwenden, um die aktuelle Position im Textfeld anzuzeigen.


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>So schreiben Sie Debuginformationen in eine Protokolldatei

Um das Debuggen zu aktivieren oder zu deaktivieren, ändern Sie den Wert des folgenden Registrierungsschlüssels:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Preferences \\ scriptdebugging**

Wenn Sie den Wert auf 1 festlegen, wird die Protokollierung aktiviert. Wenn Sie den Wert auf 0 (Standardeinstellung) festlegen, wird die Protokollierung deaktiviert.

Wenn die Protokollierung aktiviert ist, wird eine Datei auf dem Computer des Benutzers in demselben Ordner wie die-Skin abgelegt. Die Datei erhält den Namen "*filename* \_ 0 \_log.txt", wobei *filename* für den Namen der Skin-Datei steht. Mit dem-Design kann der Code in der Skin Text in diese Datei *schreiben.* **logstring** -Methode. Dies kann hilfreich sein, wenn Sie bestimmen möchten, was innerhalb Ihres Codes passiert, während er ausgeführt wird. Beachten Sie, dass die Textdatei mit Unicode-Zeichen codiert ist.

Wenn die Protokollierung aktiviert ist und Sie ein Entwicklungssystem installiert haben, das Debuggingfunktionen bereitstellt (z. b. Microsoft Visual Studio), bewirken Ausnahmen, die nicht von Ihrem Skriptcode behandelt werden, dass ein Debugger-Dialogfeld für jede Ausnahme geöffnet wird. Dies ist ein nützliches Feature, das Sie beim Debuggen Ihres Skriptcodes unterstützt. Außerdem können Sie den Windows-Media Player Prozess manuell an den Debugger anfügen, wenn die Protokollierung aktiviert ist.

Dieses SDK enthält eine Beispiel-Skin namens "Logging", die die Protokollierungs Funktionalität in Skins veranschaulicht. Weitere Informationen zum Verwenden der Beispiele finden Sie unter [Beispiele](samples.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Skins**](about-skins.md)
</dt> </dl>

 

 




