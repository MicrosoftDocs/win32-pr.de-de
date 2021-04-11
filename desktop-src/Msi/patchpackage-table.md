---
description: In der Tabelle patchpackage werden alle Patchpakete beschrieben, die auf dieses Produkt angewendet wurden. Für jedes Patchpaket wird der eindeutige Bezeichner für den Patch sowie Informationen zum Medien Abbild bereitgestellt, auf dem sich der Patch befindet.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Patchpakettabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218522"
---
# <a name="patchpackage-table"></a>Patchpakettabelle

In der Tabelle patchpackage werden alle Patchpakete beschrieben, die auf dieses Produkt angewendet wurden. Für jedes Patchpaket wird der eindeutige Bezeichner für den Patch sowie Informationen zum Medien Abbild bereitgestellt, auf dem sich der Patch befindet.

Die patchpakettabelle enthält die folgenden Spalten.



| Spalte  | Typ                   | Schlüssel | Nullwerte zulässig |
|---------|------------------------|-----|----------|
| PatchID | [GUID](guid.md)       | J   | N        |
| Medien\_ | [Integer](integer.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchID
</dt> <dd>

Diese Spalte enthält einen eindeutigen Bezeichner für diesen Patch.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Medien\_
</dt> <dd>

Diese Spalte ist ein Fremdschlüssel für die DiskId-Spalte der [Medien Tabelle](media-table.md) und gibt den Datenträger an, der das Patchpaket enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die patchpakettabelle ist in jedem Patchpaket erforderlich. Wenn die Tabelle fehlt, tritt beim Versuch, den Patch zu installieren, ein Fehler auf: "Fehler 2768: die Transformation im Patchpaket ist ungültig." Diese Tabelle wird normalerweise durch eine Transformation aus einem Patchpaket zum Installationspaket hinzugefügt. Sie wird in der Regel nicht direkt in ein Installationspaket verfasst.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



