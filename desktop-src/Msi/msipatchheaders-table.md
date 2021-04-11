---
description: Die msipatchheaders-Tabelle enthält die binären patchheader-Datenströme, die für die patchvalidierung verwendet werden.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Msipatchheaders-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216359"
---
# <a name="msipatchheaders-table"></a>Msipatchheaders-Tabelle

Die msipatchheaders-Tabelle enthält die binären patchheader-Datenströme, die für die patchvalidierung verwendet werden.

Die msipatchheaders-Tabelle wird verwendet, wenn bei langen [Datei Tabellen](file-table.md) Schlüsseln ein Fehler beim Generieren des patchheader-Streams in der [patchtabelle](patch-table.md)auftritt. Dies kann an der in [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)beschriebenen Datenstrom-namens Einschränkung liegen. In diesem Fall kann die patchtabelle auf die msipatchheaders-Tabelle verweisen, um den Patch-Header Datenstrom zu erstellen.

Die msipatchheaders-Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Streamref | [Bezeichner](identifier.md) | J   | N        |
| Header    | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>Streamref
</dt> <dd>

Der Primärschlüssel für die Tabelle, die einen bestimmten patchheader eindeutig identifiziert.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header
</dt> <dd>

Diese Spalte ist der binäre Stream-patchheader, der für die patchvalidierung verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird von der [Aktion PATCHFILES](patchfiles-action.md)verarbeitet. Diese Tabelle wird normalerweise durch eine Transformation aus einem Patchpaket zum Installationspaket hinzugefügt. Sie wird in der Regel nicht direkt in ein Installationspaket verfasst.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



