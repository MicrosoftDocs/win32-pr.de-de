---
title: DownloadCollection-Objekt
description: DownloadCollection-Objekt
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player Onlineshops, DownloadCollection-Objekt
- Onlineshops, DownloadCollection-Objekt
- Geben Sie 2 Onlineshops ein,DownloadCollection-Objekt
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565ddce120d71ab9825c424fefb6f0e3ace9a6ac349e87e044e9c74e6da28789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902020"
---
# <a name="downloadcollection-object"></a>DownloadCollection-Objekt

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **DownloadCollection-Objekt** enthält Eigenschaften und Methoden zum Verarbeiten von Auflistungen von Downloadelementen. Sie kann von Webseiten verwendet werden, die im vollständigen Modus Windows Media Player gehostet werden und Zugriff auf das **externe** Objekt haben, z. B. Onlineshops.

Das **DownloadCollection-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                              | BESCHREIBUNG                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Ruft die Anzahl ausstehender Downloads ab.   |
| [id](downloadcollection-id.md)       | Ruft die ID der Downloadsammlung ab. |



 

Das **DownloadCollection-Objekt** unterstützt die folgenden Methoden.



| Methode                                                | BESCHREIBUNG                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Clear](downloadcollection-clear.md) (Deaktiviert)                 | Entfernt alle Elemente aus einer Downloadsammlung. |
| [item](downloadcollection-item.md)                   | Ruft ein ausstehendes Downloadobjekt ab.          |
| [removeItem](downloadcollection-removeitem.md)       | Entfernt ein Downloadelement aus einer Sammlung.    |
| [startDownload](downloadcollection-startdownload.md) | Reiht einen Download in die Warteschlange ein.                            |



 

Der Zugriff auf das **DownloadCollection-Objekt** erfolgt über die folgenden Methoden.



| Object                                        | Methode                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

Zur Veranschaulichung **laden Sie DownloadManager** herunter. **getDownloadCollection**(*collectionId*) wird in den Abschnitten zur Verweissyntax verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




