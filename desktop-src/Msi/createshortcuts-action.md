---
description: Die CreateShortcuts-Aktion verwaltet die Erstellung von Verknüpfungen.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: CreateShortcuts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209dbd38d64abb2ddedb267512dd3872991d58071769d25606ed364a15c6d958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649740"
---
# <a name="createshortcuts-action"></a>CreateShortcuts-Aktion

Die CreateShortcuts-Aktion verwaltet die Erstellung von Verknüpfungen.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die CreateShortcuts-Aktion muss nach der [InstallFiles-Aktion](installfiles-action.md) und der [RemoveShortcuts-Aktion](removeshortcuts-action.md) angegeben werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten      |
|-------|---------------------------------|
| \[1\] | Bezeichner der erstellten Verknüpfung. |



 

## <a name="remarks"></a>Hinweise

Die CreateShortcuts-Aktion erstellt Verknüpfungen zu den Schlüsseldateien von Komponenten von Features, die für die Installation oder Ankündigung ausgewählt sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verknüpfungstabelle](shortcut-table.md)
</dt> <dt>

[MsiShortcutProperty-Tabelle](msishortcutproperty-table.md)
</dt> </dl>

 

 



