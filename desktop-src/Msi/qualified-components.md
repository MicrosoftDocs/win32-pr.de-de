---
description: Eine qualifizierte Komponente ist eine Methode der Deskription auf einer einzelnen Ebene, ähnlich wie ein Zeiger.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Qualifizierte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c9a5ccd757516402a951afa3a105d51e3a0b3d22a88614983997dbcd6d07f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376303"
---
# <a name="qualified-components"></a>Qualifizierte Komponenten

Eine qualifizierte Komponente ist eine Methode der Deskription auf einer einzelnen Ebene, ähnlich wie ein Zeiger. Qualifizierte Komponenten werden hauptsächlich verwendet, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppen. Wenn beispielsweise in der Tabelle Komponente 30 Komponenten aufgeführt sind, bei denen es sich um dieselbe Microsoft Word-Faxvorlage handelt, die in 30 Sprachen lokalisiert ist, können Sie diese mithilfe der [PublishComponent-Tabelle](publishcomponent-table.md)in einer Kategorie qualifizierter Komponenten gruppiert werden. [](component-table.md)

Qualifizierte Komponenten werden in der Tabelle Komponente auf die gleiche Weise wie normale Komponenten eingegeben. Jede Komponente muss über eine eindeutige Komponenten-ID-GUID und einen Komponentenbezeichner verfügen, die in der Tabelle Komponente angegeben sind. Darüber hinaus werden qualifizierte Komponenten einer Kategorie-GUID und einem Textzeichenfolgenqualifizierer in der PublishComponent-Tabelle zugeordnet. Auf qualifizierte Komponenten wird von der Kategorie-GUID und dem Qualifizierer verwiesen, der nur auf die normale Komponente in der Tabelle Komponente verweist.

Beispielsweise kann eine qualifizierte Komponenten-ID-GUID auf verschiedene Sprachversionen einer Ressourcen-DLL verweisen. In diesem Fall besteht die Gruppe lokalisierter Ressourcen-DLLs aus der Kategorie, und die Zeichenfolgen für numerische Locale Identifier (LCID) werden häufig als Qualifizierer verwendet. Ein Entwickler könnte ein Installationspaket erstellen, das diese qualifizierten Komponenten für folgende Aufgaben verwendet:

-   Suchen Sie den Pfad zu einer bestimmten Sprachversion der Ressourcen-DLL mit [**msiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) oder [**MsiProvideQualifiedComponentEx,**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) und installieren Sie die Ressource.
-   Ermitteln Sie alle Sprachversionen der Ressourcen-DLL, die vorhanden sind, indem Sie [**MsiEnumComponentQualifiers aufrufen.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
-   Bereiten Sie die Anwendung für die Unterstützung zusätzlicher Sprachen vor. Ein zukünftiges Sprachpaket für die Anwendung kann die qualifizierte Komponente verwenden, um weitere Sprachversionen der Ressourcen-DLL hinzuzufügen.

Weitere Informationen finden Sie unter [Verwenden von qualifizierten Komponenten.](using-qualified-components.md)

 

 



