---
title: Verweisen auf Skins in URLs
description: Verweisen auf Skins in URLs
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Windows Media Player Skins, URL-Verweise
- Skins, URL-Verweise
- URL-Verweise in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714046"
---
# <a name="referencing-skins-in-urls"></a>Verweisen auf Skins in URLs

Wenn Sie eine-URL zum Laden einer Mediendatei verwenden, die von Windows Media Player abgespielt wird, können Sie anfordern, dass eine bestimmte Skin mit dieser Datei verwendet wird. Wenn das Skin bereits auf dem Computer des Benutzers installiert ist, wird es verwendet. Andernfalls wird das vorherige Skin verwendet.

Fügen Sie am Ende der URL Folgendes ein, um eine Skin anzufordern:


```C++
?WMPSkin=skinname
```



" *Skinname* " ist der Name der Skin, die Sie anfordern möchten. Verwenden Sie keine Anführungszeichen um den Namen der Skin.

Geben Sie z. b. die folgende http-URL ein, um die Verwendung von Headspace Skin anzufordern:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Skins**](about-skins.md)
</dt> </dl>

 

 




