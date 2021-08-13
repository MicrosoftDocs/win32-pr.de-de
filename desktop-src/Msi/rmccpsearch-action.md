---
description: Die RMCCPSearch-Aktion verwendet Dateisignaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgradeinstallation durchgeführt wird.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: RMCCPSearch-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d18431a6806d055c824bf51331d6390a6f669100aa9a33db9665b9d7b37008c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625899"
---
# <a name="rmccpsearch-action"></a>RMCCPSearch-Aktion

Die RMCCPSearch-Aktion verwendet Dateisignaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgradeinstallation durchgeführt wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RMCCPSearch-Aktion sollte in der [InstallUISequence-Tabelle](installuisequence-table.md) und der [InstallExecuteSequence-Tabelle erstellt werden.](installexecutesequence-table.md) Das Installationsprogramm verhindert, dass RMCCPSearch in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Für die RMCCPSearch-Aktion muss die [**EIGENSCHAFT DRIVE \_ DRIVE**](ccp-drive.md) auf [](v-gly.md) den Stammpfad auf dem Wechseldatenträger festgelegt werden, auf dem die Installation für eines der qualifizierenden Produkte installiert ist.

Jede Dateisignatur in der TABELLE "SIGNATURESearch" wird mithilfe der [DrLocator-Tabelle](drlocator-table.md) unter dem Pfad gesucht, auf den durch die [**EIGENSCHAFT DRIVE drive \_**](ccp-drive.md) verwiesen wird. Das Fehlen der Signatur in der [Signaturtabelle](signature-table.md) gibt ein Verzeichnis an. Wenn festgestellt wird, dass eine Signatur vorhanden ist, wird die RMCCPSearch-Aktion beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TABELLE "SOLLSUCHE"](ccpsearch-table.md)
</dt> </dl>

 

 



