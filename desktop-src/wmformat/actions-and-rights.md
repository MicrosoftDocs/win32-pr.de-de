---
title: Aktionen und Rechte
description: Aktionen und Rechte
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Aktionen
- DRM (Digital Rights Management), Aktionen
- Digital Rights Management (DRM), Rechte
- DRM (Digital Rights Management), Rechte
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036430"
---
# <a name="actions-and-rights"></a>Aktionen und Rechte

Wenn eine Datei mithilfe von Windows Media DRM geschützt wird, ist ihre Verwendung vollständig eingeschränkt. Lizenzen können ausgestellt werden, um es einem Benutzer zu ermöglichen, den Inhalt auf bestimmte Weise zu verwenden. Jede Art, in der ein Benutzer den Inhalt verwenden kann, wird durch eine Aktion beschrieben. Die Wiedergabe einer Datei auf einem Computer ist beispielsweise eine Aktion.

Eine Lizenz, die eine bestimmte Aktion ermöglicht, wird als Recht zum Erteilen einer Berechtigung bezeichnet. Beispielsweise kann eine Lizenz das Recht zum Abspielen von Inhalten auf einem Computer erteilen.

Aktionen und Rechte verweisen auf die gleichen Methoden wie zum Verwenden von Inhalt. Der Unterschied besteht darin, dass sich die-Aktion auf die Verwendung bezieht, während sich die Rechte auf die Berechtigung bezieht. Trotz dieser Unterscheidung werden die Wörter Action und Right häufig austauschbar in dieser Dokumentation und in anderen Dokumenten verwendet, in denen Windows Media DRM beschrieben wird.

Die Aktionen, die von Windows Media DRM-rechten gesteuert werden, sind im Abschnitt [Rechte Konstanten](rights-constants.md) dieser Dokumentation aufgeführt.

Bestimmte Methoden der erweiterten APIs des Windows Media DRM-Clients verwenden verschiedene Konstanten, um auf die grundlegenden DRM-Rechte zu verweisen. Beispielsweise verwendet die [**iwmdrmlicensequery:: querylicensestate**](iwmdrmlicensequery-querylicensestate.md) -Methode eine Reihe von Zeichen folgen, die für die Lizenz Zustände spezifisch sind. Obwohl diese Konstanten andere Zeichen folgen als die grundlegenden Rechte Konstanten definieren, verweisen Sie auf die gleichen Rechte in der Lizenz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](drmconcepts.md)
</dt> </dl>

 

 




