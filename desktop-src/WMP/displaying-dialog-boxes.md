---
title: Anzeigen von Dialogfeldern
description: Anzeigen von Dialogfeldern
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player Onlineshops,Anzeigen von Dialogfeldern
- Onlineshops, Anzeigen von Dialogfeldern
- Geben Sie 1 Onlineshops ein, und zeigen Sie Dialogfelder an.
- Windows Media Player Onlineshops, Dialogfelder
- Onlineshops, Dialogfelder
- Geben Sie 1 Onlineshops ein, Dialogfelder
- Anzeigen von Dialogfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e71d177e7675822b1f2704bf62776e598c2e817d583020b0df962347dac4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997270"
---
# <a name="displaying-dialog-boxes"></a>Anzeigen von Dialogfeldern

Der Onlineshop kann Dialogfelder über Windows Media Player aufrufen. Rufen Sie hierzu [External.showPopup](external-showpopup.md) aus dem Skriptcode der Ermittlungsseite auf, und geben Sie einen benutzerdefinierten Indexwert an, der das anzuzeigende Dialogfeld darstellt. Dieser Indexwert hat nur für den Code des Onlineshops eine Bedeutung. Windows Media Player interpretiert diesen Wert nicht. Windows Media Player ruft dann [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)auf und übergibt g \_ szItemInfo \_ PopupURL für den *bstrInfoName-Parameter* und die Indexnummer für den *pContext-Parameter.* Das Plug-In gibt dann einen **BSTR** zurück, der die URL der Webseite enthält, die im Dialogfeld angezeigt werden soll, und der Player zeigt das Dialogfeld an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




