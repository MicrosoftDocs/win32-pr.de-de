---
title: Inhaltscontainer
description: Inhaltscontainer
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player Onlineshops, Inhaltscontainer
- Onlineshops, Inhaltscontainer
- Geben Sie 1 Onlineshops, Inhaltscontainer ein.
- Windows Media Player Onlineshops, IWMPContentContainer-Schnittstelle
- Onlineshops, IWMPContentContainer-Schnittstelle
- Geben Sie 1 Onlineshops ein, IWMPContentContainer-Schnittstelle
- Windows Media Player,Inhaltscontainer
- Windows Media Player,IWMPContentContainer-Schnittstelle
- Inhaltscontainer
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c582a04bd37e54a40f952402343c09fb7243fc07377ef7f507cc76f11390357c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123680"
---
# <a name="content-containers"></a>Inhaltscontainer

Windows Media Player verwendet Inhaltscontainer, um digitale Medieninhalte in einer Abonnementdownload- oder Kauftransaktion darzustellen. Ein Inhaltscontainer wird durch die **IWMPContentContainer-Schnittstelle** dargestellt. Ein Inhaltscontainer kann eine Liste verwandter Inhalte enthalten, z. B. ein Album, oder eine Reihe von nicht verknüpften Inhaltselementen oder *verfolgt* nach. Sie können die **IWMPContentContainer-Schnittstelle** verwenden, um die Spuren des Inhaltscontainers aufzuzählen und den Preis für jede Spur abzurufen. Sie können auch Informationen zum Inhaltscontainer selbst abrufen, z. B. die Container-ID, den Typ des Inhalts im Container und den Gesamtpreis für die Spuren im Container (der sich von der Summe der Preise der einzelnen Spuren unterscheiden kann, wie bei einem Albumkauf).

Um einen Mechanismus zum Packen mehrerer Inhaltscontainer in ein einzelnes Objekt bereitzustellen, unterstützt Windows Media Player die **IWMPContentContainerList-Schnittstelle.** **IWMPContentContainerList** stellt Methoden zum Auflisten und Abrufen der Inhaltscontainer in der Liste bereit. Um zu ermitteln, ob die Inhaltscontainerliste einen Kauf oder einen Abonnementdownload darstellt, rufen [Sie IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) auf, um einen [WMPTransactionType-Wert](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentContainer-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**IWMPContentContainerList-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




