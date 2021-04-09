---
title: Download Manager-Objekt
description: Download Manager-Objekt
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Online Stores, Download Manager-Objekt
- Online Stores, Download Manager-Objekt
- Typ 2 Online Stores, Download Manager-Objekt
- Download Manager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856347"
---
# <a name="downloadmanager-object"></a>Download Manager-Objekt

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **Download Manager** -Objekt ist das Stamm Objekt für den Windows Media Player Download-Manager. Sie kann von Webseiten verwendet werden, die in den Aufgabenbereichen des Online Store Service gehostet werden.

Das **Download Manager** -Objekt unterstützt die folgenden Methoden.



| Methode                                                                   | BESCHREIBUNG                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| ["kreatedownloadcollection"](downloadmanager-createdownloadcollection.md) | Erstellt eine leere Download Auflistung.        |
| [getdownloadcollection](downloadmanager-getdownloadcollection.md)       | Ruft die angegebene Download Auflistung ab. |



 

Der Zugriff auf das **Downloadmanager** -Objekt erfolgt über " **extern". Download Manager**. Zu Veranschaulichung wird davon ausgegangen, dass dieser Wert einer Variablen mit dem Namen "Download Manager" zugewiesen wurde, die zur Identifizierung dieses Objekts in den Abschnitten der Verweis Syntax verwendet wird.

In Windows Media Player 10 oder höher sind die **Download Manager** -Eigenschaft und das-Objekt nur über Aufgabenbereiche des Online Store Service zugänglich. Sie können den **Download Manager** nicht aus anderen Features verwenden, bei denen das **externe** Objekt verfügbar ist, z. b. HtmlView, Info Center View und Album-Informationen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




