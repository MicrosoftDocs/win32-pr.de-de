---
description: In der Tabelle "Billboard" sind die in der vollständigen Benutzeroberfläche angezeigten Karten Steuerelemente aufgeführt.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabelle "Billboard"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959504"
---
# <a name="billboard-table"></a>Tabelle "Billboard"

In der Tabelle "Billboard" sind die in der vollständigen Benutzeroberfläche angezeigten Karten Steuer [Elemente](billboard-control.md) aufgeführt.

Die Tabelle "Billboard" weist die folgenden Spalten auf.



| Spalte    | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------|-----|----------|
| Billboard | [Bezeichner](identifier.md) | J   | N        |
| Funktion\_ | [Bezeichner](identifier.md) | N   | N        |
| Aktion    | [Bezeichner](identifier.md) | N   | J        |
| Sortieren  | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard
</dt> <dd>

Der Name des [Billboard-Steuer](billboard-control.md)Elements.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Merkmals Tabelle](feature-table.md). Das Billboard wird nur angezeigt, wenn dieses Feature installiert wird.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Der Name einer Aktion. Das Billboard wird während der von dieser Aktion empfangenen Fortschrittsmeldungen angezeigt.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Stelle
</dt> <dd>

Wenn mehr als ein Billboard einer Aktion entspricht, werden diese in der von dieser Spalte definierten Reihenfolge angezeigt. Diese Zahl darf nicht negativ sein.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



