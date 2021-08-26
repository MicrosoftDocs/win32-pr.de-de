---
title: Informationen zu Error- und ErrorItem-Objekten
description: Informationen zu Error- und ErrorItem-Objekten
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player,Error-Objekt
- Windows Media Player-Objektmodell, Error-Objekt
- Objektmodell,Error-Objekt
- Windows Media Player ActiveX-Steuerelement, Error-Objekt
- ActiveX-Steuerelement, Error-Objekt
- Windows Media Player Mobiles ActiveX-Steuerelement, Error-Objekt
- Windows Media Player Mobiles,Error-Objekt
- Error-Objekt
- Windows Media Player,ErrorItem-Objekt
- Windows Media Player-Objektmodell, ErrorItem-Objekt
- Objektmodell,ErrorItem-Objekt
- Windows Media Player ActiveX-Steuerelement, ErrorItem-Objekt
- ActiveX-Steuerelement, ErrorItem-Objekt
- Windows Media Player Mobiles ActiveX-Steuerelement, ErrorItem-Objekt
- Windows Media Player Mobiles ErrorItem-Objekt
- ErrorItem-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84dcd8e0961007c185640b32ac53d249d2e739ca5e1aa4247a6735e09b2a3242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004400"
---
# <a name="about-the-error-and-erroritem-objects"></a>Informationen zu Error- und ErrorItem-Objekten

Die **Error-** und **ErrorItem-Objekte** steuern die Fehlerbehandlungsfunktionen von Windows Media Player. Das **Error-Objekt** wird über die **Error-Eigenschaft** aus dem **Player-Objekt** abgerufen. Sie können einen bestimmten Code aus dem **Error-Objekt** abrufen, indem Sie die **Item-Eigenschaft** des **Error-Objekts** verwenden, um das **ErrorItem-Objekt** zu erstellen. Geben Sie beispielsweise Folgendes ein, um den Fehlercode des ersten Fehlerelements abzurufen:


```C++
myerrorcode = player.error.item(0).errorCode;

```



Sie können die Webhilfe auch mit dem **Error-Objekt** aufrufen, indem Sie den folgenden Code verwenden:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Error-Objekt**](error-object.md)
</dt> <dt>

[**ErrorItem-Objekt**](erroritem-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




