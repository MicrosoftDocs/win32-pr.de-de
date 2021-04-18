---
title: Download Collection-Objekt
description: Download Collection-Objekt
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player Online Stores, Download Collection-Objekt
- Online Stores, downloadcollection-Objekt
- Typ 2 Online Stores, downloadcollection-Objekt
- Download Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339216"
---
# <a name="downloadcollection-object"></a>Download Collection-Objekt

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **downloadcollection** -Objekt enthält Eigenschaften und Methoden zum Verarbeiten von Auflistungen von Download Elementen. Sie kann von Webseiten verwendet werden, die im vollständigen Windows-Media Player gehostet werden und Zugriff auf das **externe** Objekt haben, z. b. Online Stores.

Das **downloadcollection** -Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                              | BESCHREIBUNG                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Ruft die Anzahl der ausstehenden Downloads ab.   |
| [id](downloadcollection-id.md)       | Ruft die ID der Download Auflistung ab. |



 

Das **downloadcollection** -Objekt unterstützt die folgenden Methoden.



| Methode                                                | BESCHREIBUNG                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Löschen](downloadcollection-clear.md)                 | Entfernt alle Elemente aus einer Download Auflistung. |
| [item](downloadcollection-item.md)                   | Ruft ein ausstehendes Download Objekt ab.          |
| [RemoveItem](downloadcollection-removeitem.md)       | Entfernt ein Download Element aus einer Sammlung.    |
| [startDownload](downloadcollection-startdownload.md) | Fügt einen Download in die Warteschlange                            |



 

Der Zugriff auf das **downloadcollection** -Objekt erfolgt über die folgenden Methoden.



| Object                                        | Methode                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [Download Manager](downloadmanager-object.md) | ["kreatedownloadcollection"](downloadmanager-createdownloadcollection.md) |
| [Download Manager](downloadmanager-object.md) | [getdownloadcollection](downloadmanager-getdownloadcollection.md)       |



 

Zum Zweck der Veranschaulichung **Download Manager**. **getdownloadcollection**(*CollectionId*) wird in den Abschnitten der Verweis Syntax verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




