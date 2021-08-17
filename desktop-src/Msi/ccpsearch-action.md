---
description: Die AKTION DURCHSUCHE verwendet Dateisignaturen, um zu überprüfen, ob qualifizierende Produkte auf einem System installiert sind, bevor eine Upgradeinstallation durchgeführt wird.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: ACTION FORSEARCH (AKTION)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201af22dd557541825dcf2c47f06e7cf67cd8785fa85e0b78a28c25a570ffc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145693"
---
# <a name="ccpsearch-action"></a>ACTION FORSEARCH (AKTION)

Die AKTION DURCHSUCHE verwendet Dateisignaturen, um zu überprüfen, ob qualifizierende Produkte auf einem System installiert sind, bevor eine Upgradeinstallation durchgeführt wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

DIEAKTIONSEARCH-Aktion sollte in der [InstallUISequence-Tabelle](installuisequence-table.md) und der [InstallExecuteSequence-Tabelle erstellt werden.](installexecutesequence-table.md) Das Installationsprogramm verhindert, dass die AKTION "INSTALLERSearch" in der Sequenz InstallExecuteSequence ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde. Die AKTION RMSearch muss vor der [RMCCPSearch-Aktion](rmccpsearch-action.md) kommen.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

Mit der AKTION SIGNATURESearch wird anhand der folgenden Tabellen nach dateisignierten Signaturen gesucht, die in der TABELLE DES SYSTEMS aufgeführt sind: Signature, CompLocator, RegLocator, IniLocator und DrLocator.

Wenn festgestellt wird, dass eine Signatur vorhanden ist, wird die **SUCCESS \_ Success-Eigenschaft** auf 1 festgelegt, und die AKTION VOM SUCH-Objekt wird beendet.

Das Fehlen der Signatur in der Signaturtabelle gibt ein Verzeichnis an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CCPSearch](ccpsearch-table.md)
</dt> <dt>

[Signature](signature-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



