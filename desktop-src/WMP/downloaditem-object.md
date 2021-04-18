---
title: Download Item-Objekt
description: Download Item-Objekt
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player Online Stores, Downloader-Objekt
- Online Stores, Download Item-Objekt
- Typ 2 Online Stores, Downloader-Objekt
- Download Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337393"
---
# <a name="downloaditem-object"></a>Download Item-Objekt

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **downloadaditem** -Objekt stellt eine Datei Download Anforderung dar. Sie kann von Webseiten verwendet werden, die im vollständigen Windows-Media Player gehostet werden und Zugriff auf das **externe** Objekt haben, z. b. Premium-Dienste.

Das Objekt " **Downloader** " unterstützt die folgenden Eigenschaften.



| Eigenschaft                                        | BESCHREIBUNG                                      |
|-------------------------------------------------|--------------------------------------------------|
| [Download Status](downloaditem-downloadstate.md) | Ruft den Status des Downloads ab.             |
| [Progress](downloaditem-progress.md)           | Ruft den Fortschritt des Downloads in Bytes ab. |
| [size](downloaditem-size.md)                   | Ruft die Größe des Downloads ab.              |
| [SourceURL](downloaditem-sourceurl.md)         | Ruft die Quell-URL des Downloads ab.        |
| [type](downloaditem-type.md)                   | Ruft den Typ des Downloads ab.              |



 

Das Objekt " **Downloader** " unterstützt die folgenden Methoden.



| Methode                                      | BESCHREIBUNG                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Bricht den Download ab.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Ruft den Wert eines Attributs für das Download Element ab. |
| [pause](downloaditem-pause.md)             | Hält den Download an.                                       |
| [zusetzen](downloaditem-resume.md)           | Der Download wird fortgesetzt.                                      |



 

Der Zugriff auf das **Download** Item-Objekt erfolgt über die folgende Eigenschaft.



| Object                                              | Eigenschaft                            |
|-----------------------------------------------------|-------------------------------------|
| [Download Sammlung](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

Zum Zweck der Veranschaulichung **Download Manager**. **getdownloadcollection**(*CollectionId*). **Item**(*ItemID*) wird in den Abschnitten der Verweis Syntax verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




