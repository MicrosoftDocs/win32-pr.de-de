---
title: Überlegungen zu internationalen Märkten
description: Überlegungen zu internationalen Märkten
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player Onlineshops,internationale Märkte
- Onlineshops,internationale Märkte
- Typ 1 Onlineshops,internationale Märkte
- Typ 2 Onlineshops,internationale Märkte
- Internationale Märkte
- Windows Media Player,ServiceInfo-Dokument
- Onlineshops,ServiceInfo-Dokument
- Typ 1 Onlineshops,ServiceInfo-Dokument
- Typ 2 Onlineshops,ServiceInfo-Dokument
- ServiceInfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e2db056f748e1257649716c57a2f1774ee0b1b149966dce3851a75d08c8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580510"
---
# <a name="considerations-for-international-markets"></a>Überlegungen zu internationalen Märkten

Wenn Ihr Unternehmen Onlineshops für mehrere Märkte erstellt, müssen Sie Microsoft die URL eines ServiceInfo-Dokuments für jeden Markt bereitstellen. Sie können dies auf eine der beiden folgenden Arten tun:

-   Erstellen Sie ein separates ServiceInfo-Dokument für jeden Markt. In diesem Fall stellen Sie Microsoft URLs zur Verfügung, die auf einzelne ServiceInfo-Dokumente für jeden Onlineshop in jedem Markt verweisen.
-   Erstellen Sie ein einzelnes ServiceInfo-Dokument für alle Märkte. Wenn Sie dies tun, stellen Sie Microsoft die gleiche URL für jeden Markt zur Verfügung. Ihr ServiceInfo-Dokument, das als ASP-Seite erstellt wurde, kann dann den Speicherort des Benutzers basierend auf Abfragezeichenfolgenparametern dynamisch erkennen.

Windows Media Player fügt eine Abfragezeichenfolge an die ServiceInfo-URL-Anforderung an, die Informationen über das Lokale und die Speicherorteinstellungen des Benutzers enthält. Wenn Ihr Onlineshop diese Informationen verwendet, um zu bestimmen, welche Inhalte angezeigt werden sollen, sollten Sie diese Werte dynamisch an Ihre eigenen URLs in Ihrem ServiceInfo-Dokument anfügen. Dies ist die beste Möglichkeit, um sicherzustellen, dass Ihre Webseiten-URLs immer die parameter enthalten, die Sie erwarten.

Nachdem Sie den Standort und die Spracheinstellung des Benutzers festgelegt haben, sollten Sie diese Informationen für zukünftige Sitzungen beibehalten. Sie können dazu eine der Verfahren verwenden, die Sie normalerweise auf einer Webseite verwenden würden, z. B. Cookies, oder indem Sie Ihr COM-Objekt verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dynamisches Erstellen des ServiceInfo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo-Element**](serviceinfo-element.md)
</dt> </dl>

 

 




