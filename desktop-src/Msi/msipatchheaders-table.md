---
description: Die MsiPatchHeaders-Tabelle enthält die binären Patchheaderstreams, die für die Patchvalidierung verwendet werden.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: MsiPatchHeaders-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1888a91da13923c4a9904c770df77cb24a5b8381c869a60895bb5ff49d23e6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944492"
---
# <a name="msipatchheaders-table"></a>MsiPatchHeaders-Tabelle

Die MsiPatchHeaders-Tabelle enthält die binären Patchheaderstreams, die für die Patchvalidierung verwendet werden.

Die MsiPatchHeaders-Tabelle wird verwendet, wenn lange [Dateitabellenschlüssel](file-table.md) zu einem Fehler beim Generieren des Patchheaderstreams in der [Patchtabelle](patch-table.md)führen. Dies kann auf die Einschränkung des Streamnamens zurückzuführen sein, die unter [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)beschrieben ist. In diesem Fall kann die Patch-Tabelle auf die MsiPatchHeaders-Tabelle verweisen, um den Patchheaderstream zu erstellen.

Die MsiPatchHeaders-Tabelle enthält die folgenden Spalten.



| Spalte    | Typ                         | Key | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identifier](identifier.md) | J   | N        |
| Header    | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

Der Primärschlüssel für die Tabelle, die einen bestimmten Patchheader eindeutig identifiziert.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header
</dt> <dd>

Diese Spalte ist der binäre Streampatchheader, der für die Patchvalidierung verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird von der [PatchFiles-Aktion](patchfiles-action.md)verarbeitet. Diese Tabelle wird dem Installationspaket in der Regel durch eine Transformation aus einem Patchpaket hinzugefügt. Er wird in der Regel nicht direkt in einem Installationspaket erstellt.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



