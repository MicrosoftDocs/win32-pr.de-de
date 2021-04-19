---
description: Die Tabelle "upgradedfilestoignore" verhindert, dass bestimmte Dateien, die tatsächlich im aktualisierten Image geändert wurden, relativ zu den Ziel Images aktualisiert werden.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabelle "Upgrade dfilestoignore" (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362961"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Tabelle "Upgrade dfilestoignore" (Patchwiz.dll)

Die Tabelle "upgradedfilestoignore" verhindert, dass bestimmte Dateien, die tatsächlich im aktualisierten Image geändert wurden, relativ zu den Ziel Images aktualisiert werden. In bestimmten Fällen ist es möglicherweise hilfreich, dies zu tun. Beispielsweise muss ein Patchpaket, das nur für die Verwendung mit nicht administrativen Installationen vorgesehen ist, keine Dateien für das Patchen enthalten, die nur Teil von administrativen Images sind. Das Ausschließen von Dateien, die nur in administrativen Images verwendet werden, kann die Größe des Patchpakets verringern. Administratoren sollten jedoch darüber informiert werden, wie Sie diese Dateien separat aktualisieren. Diese Tabelle ist in der Datenbank für die Patcherstellung (PCP-Datei) optional und wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.

Die Tabelle "Upgrade dfilestoignore" weist die folgenden Spalten auf.



| Spalte   | Typ | Schlüssel | Nullwerte zulässig |
|----------|------|-----|----------|
| Upgraded | text | J   | N        |
| FTK      | text | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Fremdschlüssel für die aktualisierte Spalte der [Tabelle "UpgradedImages" (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md). Das Tool für die Patcherstellung schließt die Aktualisierung der in der FTK-Spalte der Tabelle "upgradedfilestoignore" angegebenen Datei aus, wenn ein Ziel auf das im aktualisierten Feld angegebene Bild aktualisiert wird. Geben Sie \* im Feld aktualisiert den Wert "" ein, um das Aktualisieren der Datei auf alle aktualisierten Images auszuschließen.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in die [Dateitabelle](file-table.md) des aktualisierten Abbilds. Ein Wert im <prefix> \* Format "" entspricht allen Datei Tabellen Schlüsseln in der Dateitabelle, die mit diesem Präfix beginnen. Es kann kein Text auf das Sternchen folgen.

</dd> </dl>

 

 



