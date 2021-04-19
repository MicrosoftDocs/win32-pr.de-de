---
description: Mit der Aktion selfunregmodules werden alle in der Tabelle selfreg aufgeführten Module, deren deinstallieren geplant ist, aufgehoben. Das Installationsprogramm führt keine Selbstregistrierung durch. EXE-Dateien.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Selfunregmodules-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357073"
---
# <a name="selfunregmodules-action"></a>Selfunregmodules-Aktion

Mit der Aktion selfunregmodules werden alle in der [Tabelle selfreg](selfreg-table.md) aufgeführten Module, deren deinstallieren geplant ist, aufgehoben. Das Installationsprogramm führt keine Selbstregistrierung durch. EXE-Dateien.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate](installvalidate-action.md) -Aktion muss vor der selfunregmodules-Aktion in der Sequenz angezeigt werden. Wenn eine [SelfRegModules](selfregmodules-action.md) -Aktion verwendet wird, muss Sie nach der selfunregmodules-Aktion in der Sequenz angezeigt werden. Wenn eine [RemoveFiles-Aktion](removefiles-action.md) verwendet wird, muss Sie nach der selfunregmodules-Aktion in der Sequenz angezeigt werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                             |
|-------|--------------------------------------------------------|
| \[1\] | Bezeichner der nicht registrierten Modul Datei.                |
| \[2\] | Bezeichner des Ordners, der die nicht registrierte Modul Datei enthält. |



 

## <a name="remarks"></a>Bemerkungen

Die selfunregmodules-Aktion versucht, die [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) -Funktion des Moduls aufzurufen, dessen Registrierung aufgehoben werden soll. Diese Aktion wird mit erhöhten Rechten ausgeführt, wenn die Installation mit erweiterten Berechtigungen ausgeführt wird, z. b. während einer Installation pro Computer. Während einer Installation pro Benutzer führt das Installationsprogramm diese Aktion mit Benutzerberechtigungen aus.

Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der das Installationsprogramm die Registrierung selbst Registrierender DLLs mithilfe der selfunregmodules-Aktion aufgehoben hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
