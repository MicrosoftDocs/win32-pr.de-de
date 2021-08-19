---
description: Die SelfRegModules-Aktion verarbeitet alle module, die in der SelfReg-Tabelle aufgeführt sind, und registriert alle installierten Module beim System. Das Installationsprogramm registriert exe-Dateien nicht selbst.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: SelfRegModules-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf137dc63baa72a3d5b93370e40911af93691eaa911c4081990656c84091870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630040"
---
# <a name="selfregmodules-action"></a>SelfRegModules-Aktion

Die SelfRegModules-Aktion verarbeitet alle module, die in der [SelfReg-Tabelle](selfreg-table.md) aufgeführt sind, und registriert alle installierten Module beim System. Das Installationsprogramm registriert exe-Dateien nicht selbst.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss aufgerufen werden, bevor die SelfRegModules-Aktion aufgerufen wird. Wenn eine [InstallFiles-Aktion](installfiles-action.md) verwendet wird, muss sie vor der SelfRegModules-Aktion in der Sequenz angezeigt werden. Da die SelfRegModules-Aktion das System ändert, sollte SelfRegModules nach der [InstallInitialize-Aktion kommen.](installinitialize-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                           |
|-------|------------------------------------------------------|
| \[1\] | Bezeichner der registrierten Moduldatei.                |
| \[2\] | Bezeichner des Ordners, der die registrierte Moduldatei enthält. |



 

## <a name="remarks"></a>Hinweise

Die SelfRegModules-Aktion versucht, die [DllRegisterServer-Funktion](/windows/win32/api/olectl/nf-olectl-dllregisterserver) des Moduls auf aufruft, das registriert werden soll. Diese Aktion wird mit erhöhten Rechten ausgeführt, wenn die Installation mit erhöhten Rechten ausgeführt wird, z. B. während einer Installation pro Computer. Während einer benutzerspezifischen Installation führt das Installationsprogramm diese Aktion mit Benutzerberechtigungen aus.

Beachten Sie, dass Sie die Reihenfolge, in der das Installationsprogramm selbstregistrierungs-DLLs registriert, nicht mithilfe der [SelfUnRegModules-Aktion angeben können.](selfunregmodules-action.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
