---
title: Error-Objekt (WMP SDK)
description: Das Error-Objekt bietet Zugriff auf eine Auflistung von ErrorItem-Objekten.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Fehlerobjekt-Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748469"
---
# <a name="error-object"></a>Error-Objekt

Das **Error-Objekt** bietet Zugriff auf eine Auflistung von [ErrorItem-Objekten.](erroritem-object.md)

Das **Error-Objekt** unterstützt die folgende Eigenschaft.



| Eigenschaft                           | Beschreibung                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Ruft die Anzahl der Fehler in der Fehlerwarteschlange ab. |



 

Das **Error-Objekt** unterstützt die folgenden Methoden.



| Methode                                       | Beschreibung                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Entfernt die Fehler aus der Fehlerwarteschlange.                                                         |
| [item](error-item.md)                       | Ruft ein [ErrorItem-Objekt](erroritem-object.md) aus der Fehlerwarteschlange ab.                     |
| [Webhelp](error-webhelp.md)                 | Startet die Windows Media Player Webhilfeseite, um weitere Informationen zum Fehler anzuzeigen. |



 

Auf **das Error-Objekt** wird über die folgende Eigenschaft zugegriffen.



| Object                      | Eigenschaft                  |
|-----------------------------|---------------------------|
| [Player](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




