---
description: Die ccpsearch-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Ccpsearch-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356679"
---
# <a name="ccpsearch-action"></a>Ccpsearch-Aktion

Die ccpsearch-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die ccpsearch-Aktion sollte in der Tabelle " [InstallUISequence](installuisequence-table.md) " und der [Tabelle "InstallExecuteSequence](installexecutesequence-table.md)" erstellt werden. Das Installationsprogramm verhindert, dass die ccpsearch-Aktion in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde. Die ccpsearch-Aktion muss vor der [RMCCPSEARCH](rmccpsearch-action.md) -Aktion erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die ccpsearch-Aktion sucht in der folgenden Tabelle nach Datei Signaturen, die in der Tabelle ccpsearch auf dem System aufgeführt sind: Signature, complocator, reglocator, inilocator und drlocator.

Wenn eine Signatur als vorhanden festgelegt wird, wird die Eigenschaft **CCP \_ Success** auf 1 festgelegt, und die ccpsearch-Aktion wird beendet.

Das Fehlen der Signatur aus der Signatur Tabelle deutet auf ein Verzeichnis hin.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ccpsearch](ccpsearch-table.md)
</dt> <dt>

[Signature](signature-table.md)
</dt> <dt>

[Complocator](complocator-table.md)
</dt> <dt>

[Reglocator](reglocator-table.md)
</dt> <dt>

[Inilocator](inilocator-table.md)
</dt> <dt>

[Drlocator](drlocator-table.md)
</dt> </dl>

 

 



