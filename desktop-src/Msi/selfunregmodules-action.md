---
description: Mit der SelfUnregModules-Aktion wird die Registrierung aller Module aufgehoben, die in der SelfReg-Tabelle aufgeführt sind und deinstalliert werden sollen. Das Installationsprogramm registriert .EXE Dateien nicht selbst.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: SelfUnregModules-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ba95a745716d512a72e9541064f56bdc663e2e6c9658a9c35744449217952f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040330"
---
# <a name="selfunregmodules-action"></a>SelfUnregModules-Aktion

Mit der SelfUnregModules-Aktion wird die Registrierung aller Module aufgehoben, die in der [SelfReg-Tabelle](selfreg-table.md) aufgeführt sind und deinstalliert werden sollen. Das Installationsprogramm registriert .EXE Dateien nicht selbst.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss vor der SelfUnregModules-Aktion in der Sequenz angezeigt werden. Wenn eine [SelfRegModules-Aktion](selfregmodules-action.md) verwendet wird, muss sie nach der SelfUnregModules-Aktion in der Sequenz angezeigt werden. Wenn eine [RemoveFiles-Aktion](removefiles-action.md) verwendet wird, muss sie nach der SelfUnregModules-Aktion in der Sequenz angezeigt werden.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                             |
|-------|--------------------------------------------------------|
| \[1\] | Bezeichner der nicht registrierten Moduldatei.                |
| \[2\] | Bezeichner des Ordners mit nicht registrierter Moduldatei. |



 

## <a name="remarks"></a>Hinweise

Die SelfUnregModules-Aktion versucht, die [**DllUnregisterServer-Funktion**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) des Moduls aufzurufen, für das die Registrierung aufgehoben werden soll. Diese Aktion wird mit erhöhten Rechten ausgeführt, wenn die Installation mit erhöhten Rechten ausgeführt wird, z. B. während einer Computerinstallation. Während einer Benutzerinstallation führt das Installationsprogramm diese Aktion mit Benutzerberechtigungen aus.

Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der das Installationsprogramm die Registrierung selbstregistrierender DLLs mithilfe der SelfUnRegModules-Aktion aufheben kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
