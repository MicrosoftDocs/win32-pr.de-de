---
description: Mit der Aktion "Write-einivalues" werden die Informationen der INI-Datei, die von der Anwendung benötigt werden, in die INI-Dateien geschrieben.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Aktion "Write-einivalues"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866048"
---
# <a name="writeinivalues-action"></a>Aktion "Write-einivalues"

Mit der Aktion "Write-einivalues" werden die Informationen der INI-Datei, die von der Anwendung benötigt werden, in die INI-Dateien geschrieben. Das Schreiben dieser Informationen wird von der [Komponenten Tabelle](component-table.md)abgegrenzt. Ein INI-Wert wird geschrieben, wenn die entsprechende Komponente so festgelegt wurde, dass Sie entweder lokal oder über die Quelle ausgeführt wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die InstallValidate-Aktion muss vor der Aktion "Write-einivalues" erfolgen. Wenn eine [RemoveIniValues-Aktion](removeinivalues-action.md) in der Sequenz vorhanden ist, muss Sie vor der Aktion "Write" geschrieben werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten              |
|-------|-----------------------------------------|
| \[1\] | Bezeichner der INI-Datei.                |
| \[2\] | INI-Datei Schlüssel im folgenden Abschnitt. |
| \[3\] | Das Element wurde aus der INI-Datei entfernt.            |
| \[4\] | Der Wert wurde aus der INI-Datei entfernt.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[INIFILE-Tabelle](inifile-table.md)
</dt> </dl>

 

 



