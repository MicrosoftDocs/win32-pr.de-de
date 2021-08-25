---
description: In der Tabelle PatchPackage werden alle Patchpakete beschrieben, die auf dieses Produkt angewendet wurden. Für jedes Patchpaket wird der eindeutige Bezeichner für den Patch zusammen mit Informationen zum Medienimage bereitgestellt, auf dem sich der Patch befindet.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: PatchPackage-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4027913854436072330a69a788ca9dc9b1365a71b82fd1727227e33d8a203b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926120"
---
# <a name="patchpackage-table"></a>PatchPackage-Tabelle

In der Tabelle PatchPackage werden alle Patchpakete beschrieben, die auf dieses Produkt angewendet wurden. Für jedes Patchpaket wird der eindeutige Bezeichner für den Patch zusammen mit Informationen zum Medienimage bereitgestellt, auf dem sich der Patch befindet.

Die PatchPackage-Tabelle enthält die folgenden Spalten.



| Spalte  | Typ                   | Key | Nullwerte zulässig |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | J   | N        |
| Medien\_ | [Integer](integer.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

Diese Spalte enthält einen eindeutigen Bezeichner für diesen bestimmten Patch.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Medien\_
</dt> <dd>

Diese Spalte ist ein Fremdschlüssel für die DiskId-Spalte der [Medientabelle](media-table.md) und gibt den Datenträger an, der das Patchpaket enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die PatchPackage-Tabelle ist in jedem Patchpaket erforderlich. Wenn die Tabelle fehlt, schlägt der Versuch, den Patch zu installieren, mit "Fehler 2768: Transformieren im Patchpaket ist ungültig" fehl. Diese Tabelle wird dem Installationspaket in der Regel durch eine Transformation aus einem Patchpaket hinzugefügt. Er wird in der Regel nicht direkt in einem Installationspaket erstellt.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



