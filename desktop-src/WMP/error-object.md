---
title: Error-Objekt (WMP-SDK)
description: Das Error-Objekt ermöglicht den Zugriff auf eine Auflistung von ErrorItem-Objekten.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Windows-Fehler Objekt-Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2019
ms.locfileid: "106340475"
---
# <a name="error-object"></a>Error-Objekt

Das **Error** -Objekt ermöglicht den Zugriff auf eine Auflistung von [ErrorItem](erroritem-object.md) -Objekten.

Das **Error** -Objekt unterstützt die folgende Eigenschaft.



| Eigenschaft                           | BESCHREIBUNG                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Ruft die Anzahl der Fehler in der Fehler Warteschlange ab. |



 

Das **Error** -Objekt unterstützt die folgenden Methoden.



| Methode                                       | BESCHREIBUNG                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearerrorqueue](error-clearerrorqueue.md) | Löscht die Fehler in der Fehler Warteschlange.                                                         |
| [item](error-item.md)                       | Ruft ein [ErrorItem](erroritem-object.md) -Objekt aus der Fehler Warteschlange ab.                     |
| [WebHelp](error-webhelp.md)                 | Hiermit wird die Windows Media Player-Webhilfe Seite gestartet, um weitere Informationen zum Fehler anzuzeigen. |



 

Der Zugriff auf das **Fehler** Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                  |
|-----------------------------|---------------------------|
| [Player](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




