---
description: Die PublishComponents-Aktion verwaltet die Ankündigung der Komponenten aus der PublishComponent-Tabelle.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: PublishComponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840035677effff22189c357ad881c9abf2c061b169e4283037ca83df19347d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913120"
---
# <a name="publishcomponents-action"></a>PublishComponents-Aktion

Die PublishComponents-Aktion verwaltet die Ankündigung der Komponenten aus der [PublishComponent-Tabelle.](publishcomponent-table.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID, die die Komponenten-ID eines angekündigten Features darstellt. |
| \[2\] | Qualifizierer der Komponenten-ID.                                   |



 

## <a name="remarks"></a>Hinweise

Die PublishComponents-Aktion veröffentlicht alle Komponenten aus der PublishComponents-Tabelle, die zu Features gehören, die für Ankündigung oder Installation ausgewählt wurden.

 

 



