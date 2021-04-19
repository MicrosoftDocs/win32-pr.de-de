---
title: Inhalts Container
description: Inhalts Container
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player Online Stores, Inhalts Container
- Online Stores, Inhalts Container
- Typ 1 Online Stores, Inhalts Container
- Windows Media Player Online Stores, iwmpcontentcontainer-Schnittstelle
- Online Stores, iwmpcontentcontainer-Schnittstelle
- Typ 1 Online Stores, iwmpcontentcontainer-Schnittstelle
- Windows Media Player, Inhalts Container
- Windows Media Player, iwmpcontentcontainer-Schnittstelle
- Inhalts Container
- Iwmpcontentcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106342120"
---
# <a name="content-containers"></a>Inhalts Container

In Windows Media Player werden Inhalts Container verwendet, um digitale Medieninhalte in einer Abonnement Download-oder Kauftransaktion darzustellen. Ein Inhalts Container wird durch die **iwmpcontentcontainer** -Schnittstelle dargestellt. Ein Inhalts Container enthält möglicherweise eine Liste verwandter Inhalte, z. b. ein-Album oder einen Satz von nicht verknüpften Inhalts Elementen oder- *Spuren*. Sie können die **iwmpcontentcontainer** -Schnittstelle verwenden, um die Spuren des Inhalts Containers aufzulisten und den Preis für jede Spur abzurufen. Sie können auch Informationen zum Inhalts Container selbst abrufen, z. b. die Container-ID, den Typ des Inhalts im Container und den Gesamtpreis für die Spuren im Container (die sich von der Summe der Preise der einzelnen Spuren unterscheiden können, wie bei einem Album Kauf).

Um einen Mechanismus zum Verpacken mehrerer Inhalts Container in einem einzelnen Objekt bereitzustellen, unterstützt Windows Media Player die **iwmpcontentcontainerlist** -Schnittstelle. **Iwmpcontentcontainerlist** stellt Methoden zum Aufzählen und Abrufen der Inhalts Container in der Liste bereit. Um zu ermitteln, ob die Inhalts Container Liste einen Kauf oder einen Abonnement Download darstellt, rufen Sie [iwmpcontentcontainerlist:: gettransaktiontype](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) auf, um einen [wmptransaktionstyp](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) -Wert abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> <dt>

[**Iwmpcontentcontainer-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**Iwmpcontentcontainerlist-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




