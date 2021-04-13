---
title: Informationen zum DVD-Objekt
description: Informationen zum DVD-Objekt
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player, DVD-Objekt
- Windows Media Player-Objektmodell, DVD-Objekt
- Objektmodell, DVD-Objekt
- Windows Media Player ActiveX-Steuerelement, DVD-Objekt
- ActiveX-Steuerelement, DVD-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, DVD-Objekt
- Windows Media Player Mobile, DVD-Objekt
- DVD-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309303"
---
# <a name="about-the-dvd-object"></a>Informationen zum DVD-Objekt

Das **DVD** -Objekt fügt für DVD-medienspezifische Funktionen hinzu. Im Allgemeinen werden DVD-Medien wie andere digitale Medien in Windows Media Player behandelt. Beispielsweise werden DVD-Laufwerke mithilfe des **cdromcollection** -Objekts aufgelistet, und DVD-Titel und-Kapitel werden mithilfe von **Wiedergabe** Listen Objekten und **Medien** Objekten manipuliert. Einige Funktionen sind jedoch DVD-spezifisch, und das **DVD** -Objekt stellt dies bereit. Beispielsweise hat die DVD ein Konzept namens "Domäne". Zum Abrufen der aktuellen Domäne für DVD-Medien geben Sie Folgendes ein:


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




