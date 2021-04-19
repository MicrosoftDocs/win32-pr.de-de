---
description: Die SelfRegModules-Aktion verarbeitet alle in der Tabelle selfreg aufgeführten Module und registriert alle installierten Module beim System. Der Installer führt keine Selbstregistrierung von exe-Dateien durch.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: SelfRegModules-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352584"
---
# <a name="selfregmodules-action"></a>SelfRegModules-Aktion

Die SelfRegModules-Aktion verarbeitet alle in der Tabelle [selfreg](selfreg-table.md) aufgeführten Module und registriert alle installierten Module beim System. Der Installer führt keine Selbstregistrierung von exe-Dateien durch.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate](installvalidate-action.md) -Aktion muss aufgerufen werden, bevor die SelfRegModules-Aktion aufgerufen wird. Wenn eine [InstallFiles](installfiles-action.md) -Aktion verwendet wird, muss Sie vor der SelfRegModules-Aktion in der Sequenz angezeigt werden. Da die SelfRegModules-Aktion das System ändert, sollte SelfRegModules nach der [InstallInitialize-Aktion](installinitialize-action.md)erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                           |
|-------|------------------------------------------------------|
| \[1\] | Bezeichner der registrierten Modul Datei.                |
| \[2\] | Bezeichner des Ordners mit der registrierten Modul Datei. |



 

## <a name="remarks"></a>Bemerkungen

Die SelfRegModules-Aktion versucht, die [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Funktion des Moduls, das für die Registrierung geplant ist, aufzurufen. Diese Aktion wird mit erhöhten Rechten ausgeführt, wenn die Installation mit erweiterten Berechtigungen ausgeführt wird, z. b. während einer Installation pro Computer. Bei einer pro-Benutzer-Installation führt das Installationsprogramm diese Aktion mit Benutzerberechtigungen aus.

Beachten Sie, dass Sie die Reihenfolge, in der der Installer selbst Registrierungs-DLLs registriert, nicht mithilfe der [selfunregmodules-Aktion](selfunregmodules-action.md)angeben können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
