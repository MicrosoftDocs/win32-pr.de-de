---
description: Die Binärtabelle enthält die Binärdaten für Elemente wie Bitmaps, Animationen und Symbole. Die binäre Tabelle wird auch zum Speichern von Daten für benutzerdefinierte Aktionen verwendet. Weitere Informationen finden Sie unter OLE-Einschränkungen für Streams.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Binäre Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a70750193b1dc147a9b2b4cfa01bbea410f0e44b7c03f16bd1c992f118a4f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638804"
---
# <a name="binary-table"></a>Binäre Tabelle

Die Binärtabelle enthält die Binärdaten für Elemente wie Bitmaps, Animationen und Symbole. Die binäre Tabelle wird auch zum Speichern von Daten für benutzerdefinierte Aktionen verwendet. Weitere Informationen finden Sie unter [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md).

Die Tabelle Binary enthält die folgenden Spalten.



| Spalte | Typ                         | Key | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Name   | [Identifier](identifier.md) | J   | N        |
| Daten   | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Ein eindeutiger Schlüssel, der die bestimmten Binärdaten identifiziert. Wenn die Binärdaten für ein -Steuerelement verwendet werden, wird der Schlüssel in der Text -Spalte des zugeordneten Steuerelements in der [Control-Tabelle](control-table.md)angezeigt. Dieser Schlüssel muss für alle Steuerelemente eindeutig sein, die Binärdaten erfordern.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Die unformatierten Binärdaten.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE29](ice29.md)  
</dl>

 

 



