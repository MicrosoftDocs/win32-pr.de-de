---
title: Überlegungen zu internationalen Märkten
description: Überlegungen zu internationalen Märkten
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player Online Stores, internationale Märkte
- Online Stores, internationale Märkte
- Typ 1 Online Stores, internationale Märkte
- Typ 2 Online Stores, internationale Märkte
- internationale Märkte
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338203"
---
# <a name="considerations-for-international-markets"></a>Überlegungen zu internationalen Märkten

Wenn Ihr Unternehmen Online-Stores für mehrere Märkte erstellt, müssen Sie Microsoft die URL eines serviceingefo-Dokuments für jeden Markt bereitstellen. Hierfür gibt es zwei Möglichkeiten:

-   Erstellen Sie ein separates servicinput Info-Dokument für jeden Markt. In diesem Fall stellen Sie Microsoft URLs zur Verfügung, die auf einzelne serviceInfo-Dokumente für jeden Online Shop auf jedem Markt zeigen.
-   Erstellen Sie ein einzelnes serviceInfo-Dokument für alle Märkte. Wenn Sie dies tun, geben Sie Microsoft die gleiche URL für jeden Markt. Ihr serviceingefo-Dokument, das als ASP-Seite erstellt wurde, kann dann den Speicherort des Benutzers basierend auf Abfrage Zeichenfolgen-Parametern dynamisch erkennen.

Windows Media Player Fügt eine Abfrage Zeichenfolge an die serviceInfo-URL-Anforderung an, die Informationen über die Gebiets Schema-und Standorteinstellungen des Benutzers bereitstellt. Wenn Ihr Online Store diese Informationen verwendet, um zu bestimmen, welche Inhalte angezeigt werden sollen, sollten Sie diese Werte dynamisch an Ihre eigenen URLs in Ihrem serviceInfo-Dokument anfügen. Dies ist die beste Möglichkeit, um sicherzustellen, dass Ihre Webseiten-URLs immer die erwarteten Parameter enthalten.

Nachdem Sie den Speicherort und die Spracheinstellung des Benutzers bestimmt haben, können Sie diese Informationen für zukünftige Sitzungen beibehalten. Hierfür können Sie eine der Techniken verwenden, die Sie normalerweise auf einer Webseite verwenden, z. b. Cookies, oder das COM-Objekt verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dynamisches Erstellen des serviceingefo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Servicinput info-Element**](serviceinfo-element.md)
</dt> </dl>

 

 




