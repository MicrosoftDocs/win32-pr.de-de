---
description: In bestimmten Fällen kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste von eingeschränkten Windows Installer öffentlichen Eigenschaften außer Kraft setzen.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Eingeschränkte öffentliche Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350012"
---
# <a name="restricted-public-properties"></a>Eingeschränkte öffentliche Eigenschaften

Im Fall einer verwalteten Installation muss der Paket Ersteller möglicherweise einschränken, welche [öffentlichen Eigenschaften](public-properties.md) an die Serverseite übermittelt werden, und er kann von einem Benutzer geändert werden, der kein Systemadministrator ist. Einige Einschränkungen sind im allgemeinen erforderlich, um eine sichere Umgebung zu verwalten, wenn die Installation erfordert, dass das Installationsprogramm erweiterte Berechtigungen verwendet. Wenn alle der folgenden Bedingungen erfüllt sind, kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste von eingeschränkten öffentlichen Eigenschaften außer Kraft setzen:

-   Das System ist Windows 2000.
-   Der Benutzer ist kein Systemadministrator.
-   Die Anwendung oder das Produkt wird mit erhöhten Rechten installiert.

Wenn alle oben genannten Bedingungen erfüllt sind, verwendet das Installationsprogramm standardmäßig die folgende Liste der eingeschränkten öffentlichen Eigenschaften, die von jedem Benutzer geändert werden können:

-   [**Hinspiel**](action.md)
-   [**Afterreboot**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**Executemode**](executemode.md)
-   [**Fileadddefault**](fileadddefault.md)
-   [**Fileaddlocal**](fileaddlocal.md)
-   [**Fileaddsource**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**Limitui**](limitui.md)
-   [**Logaction**](logaction.md)
-   [**Nocompanyname**](nocompanyname.md)
-   [**Nomen Name**](nousername.md)
-   [**Msienforceupgradecomponentrules**](msienforceupgradecomponentrules.md)
-   [**Msiinstanceguid**](msiinstanceguid.md)
-   [**Msinewinstance**](msinewinstance.md)
-   [**Msipatchremove**](msipatchremove.md)
-   [**Patch**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**Promptrollbackcost**](promptrollbackcost.md)
-   [**Star**](reboot.md)
-   [**Installieren Sie**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**Zusetzen**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**Shortfile-Namen**](shortfilenames.md)
-   [**Kranz**](transforms.md)
-   [**Transformsatsource**](transformsatsource.md)

Der Autor eines Installationspakets kann diese Standardliste erweitern, um zusätzliche öffentliche Eigenschaften mithilfe der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft einzubeziehen.

Wenn Sie die [**enableusercontrol**](-enableusercontrol.md) -Eigenschaft oder die [System Richtlinie](system-policy.md) [enableusercontrol](enableusercontrol.md)festlegen, wird die Liste auf alle öffentlichen Eigenschaften erweitert. Alle Benutzer können dann eine beliebige öffentliche Eigenschaft ändern.

Der Installer legt die [**restrictedusercontrol**](restrictedusercontrol.md) -Eigenschaft fest, wenn die Liste der öffentlichen Eigenschaften, die von Benutzern ohne Administratorrechte an den Server übergeben werden, eingeschränkt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> </dl>

 

 



