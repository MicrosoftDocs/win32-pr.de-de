---
description: In bestimmten Fällen kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste von eingeschränkten Windows Installer-Eigenschaften außer Kraft setzen.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Eingeschränkte öffentliche Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af09200f10261e50564ae79dbad961474d23d8a6354cee7344aa107c8b73fb57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979300"
---
# <a name="restricted-public-properties"></a>Eingeschränkte öffentliche Eigenschaften

Bei einer verwalteten Installation muss der Paketautor [](public-properties.md) möglicherweise einschränken, welche öffentlichen Eigenschaften an die Serverseite übergeben werden und von einem Benutzer geändert werden können, der kein Systemadministrator ist. Einige Einschränkungen sind häufig erforderlich, um eine sichere Umgebung zu gewährleisten, wenn das Installationsprogramm erhöhte Rechte verwenden muss. Wenn alle folgenden Bedingungen erfüllt sind, kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste eingeschränkter öffentlicher Eigenschaften überschreiben:

-   Das System ist Windows 2000.
-   Der Benutzer ist kein Systemadministrator.
-   Die Anwendung oder das Produkt wird mit erhöhten Rechten installiert.

Wenn alle oben genannten Bedingungen erfüllt sind, verwendet das Installationsprogramm standardmäßig die folgende Liste eingeschränkter öffentlicher Eigenschaften, die von jedem Benutzer geändert werden können:

-   [**Aktion**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**Executeaction**](executeaction.md)
-   [**EXECUTEMODE**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**NOCOMPANYNAME**](nocompanyname.md)
-   [**NOUSERNAME**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**Patch**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**Neustart**](reboot.md)
-   [**Installieren**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**Fortsetzen**](resume.md)
-   [**Sequenz**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**Verwandelt**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

Der Autor eines Installationspakets kann diese Standardliste mithilfe der [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md) um zusätzliche öffentliche Eigenschaften erweitern.

Durch Festlegen [**der EnableUserControl-Eigenschaft**](-enableusercontrol.md) oder der [EnableUserControl-Systemrichtlinie](enableusercontrol.md)[](system-policy.md) wird die Liste auf alle öffentlichen Eigenschaften erweitert. Alle Benutzer können dann jede öffentliche Eigenschaft ändern.

Das Installationsprogramm legt die [**RestrictedUserControl-Eigenschaft**](restrictedusercontrol.md) immer dann fest, wenn die Liste der öffentlichen Eigenschaften, die von Benutzern ohne Administratorrechte an den Server übergeben werden, eingeschränkt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> </dl>

 

 



