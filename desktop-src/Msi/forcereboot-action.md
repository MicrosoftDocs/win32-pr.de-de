---
description: Mit der ForceReboot-Aktion wird der Benutzer zur Eingabe eines Neustarts des Systems während der Installation aufgefordert.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: ForceReboot-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350313"
---
# <a name="forcereboot-action"></a>ForceReboot-Aktion

Mit der ForceReboot-Aktion wird der Benutzer zur Eingabe eines Neustarts des Systems während der Installation aufgefordert. Die ForceReboot-Aktion unterscheidet sich von der [schedulereboot](schedulereboot-action.md) -Aktion darin, dass die schedulereboot-Aktion verwendet wird, um eine Aufforderung zum Neustart am Ende der Installation zu planen.

Wenn die Installation über eine Benutzeroberfläche verfügt, zeigt das Installationsprogramm bei jeder ForceReboot-Aktion ein Dialogfeld an, das den Benutzer auffordert, das System neu zu starten. Der Benutzer muss auf diese Eingabeaufforderung Antworten, bevor die Installation fortgesetzt wird. Wenn die Installation über keine Benutzeroberfläche verfügt, wird das System bei der ForceReboot-Aktion automatisch neu gestartet.

Wenn das Installationsprogramm feststellt, dass ein Neustart erforderlich ist, wird der Benutzer automatisch aufgefordert, am Ende der Installation neu zu starten, unabhängig davon, ob ForceReboot-oder schedulereboot-Aktionen in der Sequenz vorhanden sind. Beispielsweise wird das Installationsprogramm automatisch zur Eingabe eines Neustarts aufgefordert, wenn alle während der Installation verwendeten Dateien ersetzt werden müssen.

Unterdrücken Sie bestimmte Neustart Aufforderungen, indem Sie die Eigenschaft [**Neustart**](reboot.md) festlegen.

Wenn die Windows Installer während einer [Installation mit mehreren Paketen](multiple-package-installations.md)auf die Aktion ForceReboot oder [schedulereboot](schedulereboot-action.md) stößt, wird das Installationsprogramm beendet und führt ein Rollback der Installation aus. Andere Pakete, die zur Installation mit mehreren Paketen gehören und keine ForceReboot-oder schedulereboot-Aktion enthalten, können installiert werden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die folgenden Aktionen treten in der Regel als Gruppe in der Aktions Sequenz auf. Es wird empfohlen, dass die ForceReboot-Aktion nach dieser Gruppe geplant wird. Wenn die ForceReboot-Aktion vor der [registerproduct-Aktion](registerproduct-action.md)geplant wird, benötigt das Installationsprogramm erneut die Quelle des Installationspakets nach dem Neustart. Daher folgt die bevorzugte Sequenz für ForceReboot unmittelbar auf diese Aktions Sequenz.

-   [Register Product](registerproduct-action.md)
-   [Register User](registeruser-action.md)
-   [Publishproduct](publishproduct-action.md)
-   [Publishfeatures](publishfeatures-action.md)
-   ["Kreateshortcuts"](createshortcuts-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)

Die ForceReboot-Aktion muss in der Aktions Sequenz der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)zwischen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die ForceReboot-Aktion muss immer mit einer Bedingungs Anweisung verwendet werden, damit das Installationsprogramm einen Neustart nur bei Bedarf auslöst. Beispielsweise kann ein Neustart nur erforderlich sein, wenn eine bestimmte Datei ersetzt oder eine bestimmte Komponente installiert ist. Jede Produktinstallation ist eindeutig, und eine benutzerdefinierte Aktion ist möglicherweise erforderlich, um zu bestimmen, ob ein Neustart erforderlich ist. Die Bedingung für die ForceReboot-Aktion verwendet in der Regel die Eigenschaft [**afterreboot**](afterreboot.md) .

ForceReboot führt System Vorgänge aus, die von vorherigen Aktionen generiert wurden, bevor die Aufforderung zum Neustart oder Neustarten angefordert wird. Beispielsweise werden die von " [InstallFiles](installfiles-action.md) " und " [schreiteregistryvalues](writeregistryvalues-action.md) " generierten System Vorgänge vor einem Neustart ausgeführt.

Mit der ForceReboot-Aktion wird ein Registrierungsschlüssel geschrieben, der bewirkt, dass das Installationsprogramm nach einem Neustart gestartet wird. Der Speicherort dieses Schlüssels ist **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Neustarts](system-reboots.md)
</dt> </dl>

 

 



