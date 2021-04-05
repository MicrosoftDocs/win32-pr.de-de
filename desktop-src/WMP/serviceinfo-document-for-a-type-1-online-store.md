---
title: ServiceInfo-Dokument für einen Typ-1-Online Store
description: ServiceInfo-Dokument für einen Typ-1-Online Store
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037109"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>ServiceInfo-Dokument für einen Typ-1-Online Store

Typ 1 Online Stores müssen Microsoft die URL eines XML-Dokuments bereitstellen, das den Online Shop beschreibt. In Windows Media Player 11 wird dieses Dokument verwendet, um zu bestimmen, wie die Benutzeroberfläche zum Hosten des Online Stores konfiguriert wird.

Das serviceInfo-Dokument für einen Typ-1-Speicher enthält die folgenden Informationen für Windows-Media Player:

-   Informationen, die zum Konfigurieren der **Online Store-** Schaltfläche (auch als Registerkarte bezeichnet) verwendet werden, z. b. der Schaltflächen Text, die Schaltflächen Farbe und die QuickInfo für die Schaltfläche.
-   URLs für Images, die von Windows Media Player angezeigt werden, um den Online Store zu identifizieren.
-   URLs von Webseiten, die vom Online Store bereitgestellt werden, die von Windows Media Player in der Benutzeroberfläche gehostet werden.
-   URL, mit der Windows Media Player das Plug-in des Online Stores abrufen kann, damit das Plug-in auf dem Computer des Benutzers installiert werden kann.

Wenn Windows Media Player das servicanfo-Dokument aus dem Web abruft, fügt es eine Abfrage Zeichenfolge an die URL an. Die Abfrage Zeichenfolge enthält Parameter, die Informationen über das Gebiets Schema und den geografischen Standort des Benutzers sowie die Version von Windows Media Player bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> <dt>

[**Dynamisches Erstellen des serviceingefo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




