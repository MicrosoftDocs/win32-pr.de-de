---
description: Die ForceReboot-Aktion fordert den Benutzer während der Installation auf, das System neu zu starten.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: ForceReboot-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41af6b656222a31ab75c9df3f2fa9f94af415f94d6d0b50010c0b25c5742502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636071"
---
# <a name="forcereboot-action"></a>ForceReboot-Aktion

Die ForceReboot-Aktion fordert den Benutzer während der Installation auf, das System neu zu starten. Die ForceReboot-Aktion unterscheidet sich von der [ScheduleReboot-Aktion](schedulereboot-action.md) darin, dass die ScheduleReboot-Aktion verwendet wird, um eine Aufforderung zum Neustart am Ende der Installation zu planen.

Wenn die Installation über eine Benutzeroberfläche verfügt, zeigt das Installationsprogramm bei jeder ForceReboot-Aktion ein Dialogfeld an, in dem der Benutzer aufgefordert wird, das System neu zu starten. Der Benutzer muss auf diese Eingabeaufforderung reagieren, bevor er mit der Installation fortfahren kann. Wenn die Installation über keine Benutzeroberfläche verfügt, wird das System bei der ForceReboot-Aktion automatisch neu gestartet.

Wenn das Installationsprogramm feststellt, dass ein Neustart erforderlich ist, fordert es den Benutzer automatisch auf, am Ende der Installation neu zu starten, unabhängig davon, ob in der Sequenz ForceReboot- oder ScheduleReboot-Aktionen vorhanden sind. Beispielsweise fordert das Installationsprogramm automatisch einen Neustart an, wenn dateien ersetzt werden müssen, die während der Installation verwendet werden.

Unterdrücken Sie bestimmte Neustartaufforderungen, indem Sie die [**REBOOT-Eigenschaft**](reboot.md) festlegen.

Wenn der Windows Installer während einer Installation mit [mehreren Paketen](multiple-package-installations.md)auf die ForceReboot- oder [ScheduleReboot-Aktion](schedulereboot-action.md) trifft, wird das Installationsprogramm beendet und ein Rollback für die Installation unternommen. Andere Pakete, die zur Installation mehrerer Pakete gehören und keine ForceReboot- oder ScheduleReboot-Aktion enthalten, können installiert werden.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die folgenden Aktionen treten häufig zusammen als Gruppe in der Aktionssequenz auf. Es wird empfohlen, die ForceReboot-Aktion nach dieser Gruppe zu planen. Wenn die ForceReboot-Aktion vor der [RegisterProduct-Aktion](registerproduct-action.md)geplant ist, benötigt das Installationsprogramm nach dem Neustart erneut die Quelle des Installationspakets. Daher folgt die bevorzugte Sequenz für ForceReboot sofort auf diese Aktionssequenz.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

Die ForceReboot-Aktion muss zwischen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) in der Aktionssequenz der [Tabelle InstallExecuteSequence erfolgen.](installexecutesequence-table.md)

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Die ForceReboot-Aktion muss immer mit einer bedingungsbedingten Anweisung verwendet werden, sodass das Installationsprogramm nur bei Bedarf einen Neustart auslöst. Ein Neustart kann beispielsweise nur erforderlich sein, wenn eine bestimmte Datei ersetzt oder eine bestimmte Komponente installiert wird. Jede Produktinstallation ist eindeutig, und möglicherweise ist eine benutzerdefinierte Aktion erforderlich, um zu bestimmen, ob ein Neustart erforderlich ist. Die Bedingung für die ForceReboot-Aktion verwendet in der Regel die [**AFTERREBOOT-Eigenschaft.**](afterreboot.md)

ForceReboot führt Systemvorgänge aus, die von vorherigen Aktionen generiert wurden, bevor sie zur Eingabe eines Neustarts oder Neustarts aufgefordert werden. Beispielsweise werden die von [InstallFiles](installfiles-action.md) und [WriteRegistryValues generierten](writeregistryvalues-action.md) Systemvorgänge vor einem Neustart ausgeführt.

Die ForceReboot-Aktion schreibt einen Registrierungsschlüssel, der bewirkt, dass das Installationsprogramm nach dem Neustart gestartet wird. Der Speicherort dieses Schlüssels ist **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemneustarts](system-reboots.md)
</dt> </dl>

 

 



