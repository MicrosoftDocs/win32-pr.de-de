---
description: Die Tabelle UpgradedFilesToIgnore verhindert, dass bestimmte Dateien aktualisiert werden, die im aktualisierten Image relativ zu den Zielimages geändert wurden.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: UpgradedFilesToIgnore-Tabelle (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51143fcf7db350d5ee8aa1e43d49984914bcf9f05a2f8f5f787834a69b7e1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809550"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>UpgradedFilesToIgnore-Tabelle (Patchwiz.dll)

Die Tabelle UpgradedFilesToIgnore verhindert, dass bestimmte Dateien aktualisiert werden, die im aktualisierten Image relativ zu den Zielimages geändert wurden. Dies kann in bestimmten Fällen nützlich sein. Beispielsweise muss ein Patchpaket, das nur für die Verwendung mit nicht administrativen Installationen vorgesehen ist, keine Patchdateien enthalten, die nur Teil administrativer Images sind. Das Ausschließen solcher Dateien, die nur in administrativen Images verwendet werden, kann die Größe des Patchpakets verringern. Administratoren sollten jedoch darüber informiert werden, wie diese Dateien separat aktualisiert werden. Diese Tabelle ist in der Patcherstellungsdatenbank (PCP-Datei) optional und wird von der [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) verwendet.

Die Tabelle UpgradedFilesToIgnore enthält die folgenden Spalten.



| Spalte   | Typ | Key | Nullwerte zulässig |
|----------|------|-----|----------|
| Upgraded | text | J   | N        |
| FTK      | text | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aktualisiert
</dt> <dd>

Fremdschlüssel für die Spalte "Aktualisiert" der [Tabelle "UpgradedImages" (Patchwiz.dll).](upgradedimages-table-patchwiz-dll-.md) Das Tool zum Erstellen von Patches schließt das Aktualisieren der Datei aus, die in der FTK-Spalte der Tabelle UpgradedFilesToIgnore angegeben ist, wenn ein Ziel auf das im Feld Upgrade angegebene Image aktualisiert wird. Geben Sie im Feld Aktualisiert den Wert " " ein, um das \* Aktualisieren der Datei für alle aktualisierten Images auszuschließen.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Fremdschlüssel in der [Tabelle Datei des](file-table.md) aktualisierten Images. Ein Wert im Formular " <prefix> \* " entspricht allen Dateitabellenschlüsseln in der Tabelle Datei, die mit diesem Präfix beginnen. Dem Sternchen kann kein Text folgen.

</dd> </dl>

 

 



