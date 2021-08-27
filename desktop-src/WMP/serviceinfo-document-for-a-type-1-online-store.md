---
title: ServiceInfo-Dokument für eine Online-Store
description: ServiceInfo-Dokument für eine Online-Store
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player,ServiceInfo-Dokument
- Onlineshops,ServiceInfo-Dokument
- Typ 1 Onlineshops,ServiceInfo-Dokument
- ServiceInfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893cb3c849e062147d0f6bc80f3f9c1bd56a3457b60dfe30ce837820091e9710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995440"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>ServiceInfo-Dokument für eine Online-Store

Onlineshops vom Typ 1 müssen Microsoft die URL eines XML-Dokuments bereitstellen, das den Onlineshop beschreibt. Windows Media Player 11 verwendet dieses Dokument, um zu bestimmen, wie die Benutzeroberfläche zum Hosten des Onlineshops konfiguriert wird.

Das ServiceInfo-Dokument für einen Speicher vom Typ 1 enthält die folgenden Informationen für Windows Media Player:

-   Informationen zum Konfigurieren der Schaltfläche **Onlineshops** (auch als Registerkarte bezeichnet), z. B. der Schaltflächentext, die Schaltflächenfarbe und die QuickInfo für die Schaltfläche.
-   URLs für Bilder, die Windows Media Player werden, um den Onlineshop zu identifizieren.
-   URLs von Webseiten, die vom Onlineshop bereitgestellt werden und Windows Media Player hosten.
-   URL, Windows Media Player das Plug-In des Onlineshops abrufen kann, damit das Plug-In auf dem Computer des Benutzers installiert werden kann.

Wenn Windows Media Player ServiceInfo-Dokument aus dem Web abruft, wird eine Abfragezeichenfolge an die URL angefügt. Die Abfragezeichenfolge enthält Parameter, die Informationen über das Lokale und den geografischen Standort des Benutzers sowie die Version des Windows Media Player.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Dynamisches Erstellen des ServiceInfo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




