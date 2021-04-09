---
description: Die PublishComponents-Aktion verwaltet die Ankündigung der Komponenten aus der PublishComponent-Tabelle.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: PublishComponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864852"
---
# <a name="publishcomponents-action"></a>PublishComponents-Aktion

Die PublishComponents-Aktion verwaltet die Ankündigung der Komponenten aus der [PublishComponent](publishcomponent-table.md) -Tabelle.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID, die die Komponenten-ID eines angekündigten Features darstellt. |
| \[2\] | Qualifizierer der Komponenten-ID.                                   |



 

## <a name="remarks"></a>Bemerkungen

Mit der Aktion PublishComponents werden alle Komponenten aus der Tabelle PublishComponents veröffentlicht, die zu den Funktionen gehören, die für die Ankündigung oder Installation ausgewählt wurden.

 

 



