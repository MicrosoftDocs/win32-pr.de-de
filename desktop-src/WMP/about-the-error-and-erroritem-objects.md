---
title: Informationen zu den Fehlern und ErrorItem-Objekten
description: Informationen zu den Fehlern und ErrorItem-Objekten
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, Fehler Objekt
- Windows Media Player-Objektmodell, Fehler Objekt
- Objektmodell, Fehler Objekt
- Windows Media Player ActiveX-Steuerelement, Error-Objekt
- ActiveX-Steuerelement, Error-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Error-Objekt
- Windows Media Player Mobile, Fehler Objekt
- Error-Objekt
- Windows Media Player, ErrorItem-Objekt
- Windows Media Player-Objektmodell, ErrorItem-Objekt
- Objektmodell, ErrorItem-Objekt
- Windows Media Player ActiveX-Steuerelement, ErrorItem-Objekt
- ActiveX-Steuerelement, ErrorItem-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, ErrorItem-Objekt
- Windows Media Player Mobile, ErrorItem-Objekt
- ErrorItem-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310260"
---
# <a name="about-the-error-and-erroritem-objects"></a>Informationen zu den Fehlern und ErrorItem-Objekten

Die **Fehler-und** **ErrorItem** -Objekte steuern die Fehler Behandlungs Funktionen von Windows Media Player. Das **Error** -Objekt wird durch die **Error** -Eigenschaft aus dem **Player** -Objekt abgerufen. Sie können einen bestimmten Code aus dem **Error** -Objekt mit der **Item** -Eigenschaft des **Error** -Objekts erhalten, um das **ErrorItem** -Objekt zu erstellen. Um z. b. den Fehlercode des ersten Fehler Elements zu erhalten, geben Sie Folgendes ein:


```C++
myerrorcode = player.error.item(0).errorCode;

```



Mithilfe des folgenden Codes können Sie auch die Webhilfe für das **Fehler** Objekt aufrufen:


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

 

 




