---
description: Die AppSearch-Aktion verwendet Datei Signaturen, um nach vorhandenen Versionen von Produkten zu suchen.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: AppSearch-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215718"
---
# <a name="appsearch-action"></a>AppSearch-Aktion

Die AppSearch-Aktion verwendet Datei Signaturen, um nach vorhandenen Versionen von Produkten zu suchen. Mithilfe der AppSearch-Aktion können Sie ermitteln, wo Upgrades installiert werden sollen. Die AppSearch-Aktion kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert eines Registrierungs-oder INI-Datei Eintrags festzulegen.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

AppSearch sollte in der Tabelle [InstallUISequence](installuisequence-table.md) und der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)erstellt werden. Das Installationsprogramm verhindert, dass die AppSearch-Aktion in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten      |
|-------|---------------------------------|
| \[1\] | Eigenschaft, die den Datei Speicherort enthält |
| \[2\] | Datei Signatur.                 |



 

## <a name="remarks"></a>Bemerkungen

Die Aktion AppSearch erfordert, dass die [Signatur](signature-table.md) Tabelle im Installationspaket vorhanden ist. Datei Signaturen werden in der Signatur Tabelle aufgeführt. Eine Signatur, die nicht in der Signatur Tabelle ist, gibt ein Verzeichnis an, und die-Eigenschaft legt die-Eigenschaft auf den Verzeichnispfad für diese Signatur fest.

Die AppSearch-Aktion sucht zunächst mithilfe der Tabelle " [complocator](complocator-table.md) ", der Tabelle " [reglocator](reglocator-table.md) ", der Tabelle " [inilocator](inilocator-table.md) " und schließlich der Tabelle " [drlocator](drlocator-table.md) " nach Datei Signaturen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AppSearch](appsearch-table.md)
</dt> <dt>

[Complocator](complocator-table.md)
</dt> <dt>

[Inilocator](inilocator-table.md)
</dt> <dt>

[Reglocator](reglocator-table.md)
</dt> <dt>

[Drlocator](drlocator-table.md)
</dt> </dl>

 

 



