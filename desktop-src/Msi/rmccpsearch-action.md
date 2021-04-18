---
description: Die RMCCPSEARCH-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: RMCCPSEARCH-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343773"
---
# <a name="rmccpsearch-action"></a>RMCCPSEARCH-Aktion

Die RMCCPSEARCH-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die RMCCPSEARCH-Aktion sollte in der Tabelle " [InstallUISequence](installuisequence-table.md) " und der [Tabelle "InstallExecuteSequence](installexecutesequence-table.md)" erstellt werden. Das Installationsprogramm verhindert, dass RMCCPSEARCH in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die RMCCPSEARCH-Aktion erfordert [*, dass die*](v-gly.md) Eigenschaft des [**CCP- \_ Laufwerks**](ccp-drive.md) auf den Stammpfad auf dem Wechsel Datenträger festgelegt wird, der über die Installation der qualifizierenden Produkte verfügt.

Jede Datei Signatur in der ccpsearch-Tabelle wird unter dem Pfad gesucht, auf den die Eigenschaft des [**CCP- \_ Laufwerks**](ccp-drive.md) mithilfe der [drlocator](drlocator-table.md) -Tabelle verweist. Das Fehlen der Signatur aus der [Signatur](signature-table.md) Tabelle deutet auf ein Verzeichnis hin. Wenn eine Signatur so bestimmt ist, dass Sie vorhanden ist, wird die RMCCPSEARCH-Aktion beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ccpsearch-Tabelle](ccpsearch-table.md)
</dt> </dl>

 

 



