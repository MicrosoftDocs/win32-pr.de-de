---
title: DownloadItem-Objekt
description: DownloadItem-Objekt
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player,DownloadItem-Objekt
- Onlineshops,DownloadItem-Objekt
- Typ 2 Onlineshops,DownloadItem-Objekt
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfea6241e81352b8848304c3601650ef4dec2a8e5692874fa20995ccddcce38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863460"
---
# <a name="downloaditem-object"></a>DownloadItem-Objekt

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **DownloadItem-Objekt** stellt eine Dateidownloadanforderung dar. Sie kann von Webseiten verwendet werden, die im Vollmodus gehostet Windows Media Player  und Zugriff auf das Externe Objekt haben, z. B. Premium-Dienste.

Das **DownloadItem-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                        | BESCHREIBUNG                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Ruft den Status des Downloads ab.             |
| [Fortschritt](downloaditem-progress.md)           | Ruft den Fortschritt des Downloads in Bytes ab. |
| [size](downloaditem-size.md)                   | Ruft die Größe des Downloads ab.              |
| [sourceURL](downloaditem-sourceurl.md)         | Ruft die Quell-URL des Downloads ab.        |
| [type](downloaditem-type.md)                   | Ruft den Typ des Downloads ab.              |



 

Das **DownloadItem-Objekt** unterstützt die folgenden Methoden.



| Methode                                      | BESCHREIBUNG                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Bricht den Download ab.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Ruft den Wert eines Attributs für das Downloadelement ab. |
| [pause](downloaditem-pause.md)             | Hält den Download an.                                       |
| [Fortsetzen](downloaditem-resume.md)           | Setzt den Download wieder auf.                                      |



 

Der **Zugriff auf das DownloadItem-Objekt** erfolgt über die folgende Eigenschaft.



| Object                                              | Eigenschaft                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

Zur Veranschaulichung **herunterladenManager**. **getDownloadCollection**(*collectionId*). **item**(*itemId*) wird in den Abschnitten zur Referenzsyntax verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




