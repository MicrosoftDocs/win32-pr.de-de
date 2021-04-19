---
description: Die binäre Tabelle enthält die Binärdaten für Elemente wie z. b. Bitmaps, Animationen und Symbole. Die binäre Tabelle wird auch zum Speichern von Daten für benutzerdefinierte Aktionen verwendet. Siehe OLE-Einschränkungen für Datenströme.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Binäre Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349166"
---
# <a name="binary-table"></a>Binäre Tabelle

Die binäre Tabelle enthält die Binärdaten für Elemente wie z. b. Bitmaps, Animationen und Symbole. Die binäre Tabelle wird auch zum Speichern von Daten für benutzerdefinierte Aktionen verwendet. Siehe [OLE-Einschränkungen für Datenströme](ole-limitations-on-streams.md).

Die binäre Tabelle weist die folgenden Spalten auf.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Name   | [Bezeichner](identifier.md) | J   | N        |
| Daten   | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Ein eindeutiger Schlüssel, der die jeweiligen Binärdaten identifiziert. Wenn die Binärdaten für ein Steuerelement vorgesehen sind, wird der Schlüssel in der Text-Spalte des zugeordneten Steuer Elements in der [Steuerelement Tabelle](control-table.md)angezeigt. Dieser Schlüssel muss für alle Steuerelemente, die Binärdaten erfordern, eindeutig sein.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
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

 

 



