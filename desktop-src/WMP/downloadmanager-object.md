---
title: DownloadManager-Objekt
description: DownloadManager-Objekt
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Onlineshops, DownloadManager-Objekt
- Onlineshops, DownloadManager-Objekt
- Geben Sie 2 Onlineshops ein,DownloadManager-Objekt
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 500061e414d7321ed6fe4c46cafc79cd6795935847bb3d8c527364497722ecf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340524"
---
# <a name="downloadmanager-object"></a>DownloadManager-Objekt

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **DownloadManager-Objekt** ist das Stammobjekt für den Windows Media Player Download-Manager. Sie kann von Webseiten verwendet werden, die in Aufgabenbereichen des Onlineshopdiensts gehostet werden.

Das **DownloadManager-Objekt** unterstützt die folgenden Methoden.



| Methode                                                                   | BESCHREIBUNG                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Erstellt eine leere Downloadauflistung.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Ruft die angegebene Downloadauflistung ab. |



 

Auf das **DownloadManager-Objekt** wird über **external zugegriffen. DownloadManager**. Zur Veranschaulichung wird davon ausgegangen, dass dieser Wert einer Variablen namens "DownloadManager" zugewiesen wurde, die verwendet wird, um dieses Objekt in den Abschnitten zur Verweissyntax zu identifizieren.

In Windows Media Player 10 oder höher sind die **DownloadManager-Eigenschaft** und das -Objekt nur über aufgabenbereiche des Onlineshopdiensts zugänglich. Sie können **downloadManager** nicht aus anderen Features verwenden, in denen das **External-Objekt** verfügbar ist, z. B. HTMLView, Info Center-Ansicht und Albuminformationen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




