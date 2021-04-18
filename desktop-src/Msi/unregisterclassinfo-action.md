---
description: Die unregisterclassinfo-Aktion verwaltet das Entfernen von COM-Klassen Informationen aus der Systemregistrierung. Es verwendet die AppID-Tabelle.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Unregisterclassinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350970"
---
# <a name="unregisterclassinfo-action"></a>Unregisterclassinfo-Aktion

Die unregisterclassinfo-Aktion verwaltet das Entfernen von COM-Klassen Informationen aus der Systemregistrierung. Es verwendet die [AppID-Tabelle](appid-table.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die unregisterclassinfo-Aktion muss nach der [InstallInitialize](installinitialize-action.md) -Aktion und vor der [RegisterClassInfo](registerclassinfo-action.md) -Aktion erfolgen.

[Removeregistryvalues](removeregistryvalues-action.md) muss in der Sequenz vor ' unregisterclassinfo ' stehen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle angezeigt wird, müssen Sie in derselben relativen Reihenfolge wie in der folgenden Tabelle vorkommen:

-   Unregisterclassinfo
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)

So muss z. b. [RegisterExtensionInfo](registerextensioninfo-action.md) in der Sequenz Tabelle vor unregisterclassinfo stehen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten      |
|-------|---------------------------------|
| \[1\] | GUID der nicht registrierten COM-Klasse. |



 

## <a name="remarks"></a>Bemerkungen

Der Installer legt die [**oleadvtsupport**](oleadvtsupport.md) -Eigenschaft auf true fest, wenn das System des aktuellen Benutzers aktualisiert wurde, um bei Bedarf über com installieren zu können. Wenn das System die Installation von on-Demand über com nicht unterstützt, entfernt unregisterclassinfo alle in der [Klassen Tabelle](class-table.md) aufgeführten com-Klassen, die entweder den nicht installierten Features oder den von der Systemregistrierung installierten Funktionen zugeordnet sind. Andernfalls entfernt diese Aktion nur die com-Klassen, die den Funktionen zugeordnet sind, die für die Deinstallation aus der Systemregistrierung ausgewählt wurden.

 

 



