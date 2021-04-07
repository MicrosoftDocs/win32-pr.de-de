---
title: Informationen zu den CDROM-und cdromcollection-Objekten
description: Informationen zu den CDROM-und cdromcollection-Objekten
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player, cdrom-Objekt
- Windows Media Player-Objektmodell, cdrom-Objekt
- Objektmodell, cdrom-Objekt
- Windows Media Player ActiveX-Steuerelement, cdrom-Objekt
- ActiveX-Steuerelement, cdrom-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, cdrom-Objekt
- Windows Media Player Mobile, cdrom-Objekt
- Cdrom-Objekt
- Windows Media Player, cdromcollection-Objekt
- Windows Media Player-Objektmodell, cdromcollection-Objekt
- Objektmodell, cdromcollection-Objekt
- Windows Media Player ActiveX-Steuerelement, cdromcollection-Objekt
- ActiveX-Steuerelement, cdromcollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, cdromcollection-Objekt
- Windows Media Player Mobile, cdromcollection-Objekt
- Cdromcollection-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711400"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>Informationen zu den CDROM-und cdromcollection-Objekten

Die **Crom** -und **cdromcollection** -Objekte steuern die Schnittstelle zu den CD-Laufwerken Ihres Computers zum Lesen und Abspielen von CDs.

Der Zugriff auf das **cdromcollection** -Objekt erfolgt nur über die **cdromcollection** -Eigenschaft des **Player** -Objekts. Die **cdromcollection** -Eigenschaft gibt das **cdromcollection** -Objekt zurück. Sie können nur auf die Eigenschaften des **cdromcollection** -Objekts zugreifen, nachdem Sie es erstellt haben. Wenn Sie z. b. die **count** -Eigenschaft verwenden möchten, müssen Sie den folgenden Code verwenden:


```C++
mycount = player.cdromcollection.count;
```



Sie können nur über das **cdromcollection** -Objekt auf das **CDROM** -Objekt zugreifen. Wenn Sie z. b. die CD mithilfe der **auswerfen** -Methode auswerfen möchten, müssen Sie zuerst das Sammlungsobjekt und dann ein Element im-Objekt erstellen. Verwenden Sie zum Auswerfen der CD den folgenden Code:


```C++
player.cdromcollection.item(0).eject();
```



In beiden Fällen erstellen Sie zuerst das Auflistungs Objekt (**cdromcollection**) und dann ein bestimmtes Objekt dieser Sammlung. Das-Objekt ist das erste Element in der Auflistung, **Element**(0), das dem ersten CD-Laufwerk entspricht. Anschließend wird die Methode **eject** für dieses Element aufgerufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cdrom-Objekt**](cdrom-object.md)
</dt> <dt>

[**Cdromcollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




