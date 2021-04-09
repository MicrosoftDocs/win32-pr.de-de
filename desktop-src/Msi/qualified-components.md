---
description: Eine qualifizierte Komponente ist eine Methode der Dereferenzierung auf einzelner Ebene, ähnlich wie ein-Zeiger.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Qualifizierte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864847"
---
# <a name="qualified-components"></a>Qualifizierte Komponenten

Eine qualifizierte Komponente ist eine Methode der Dereferenzierung auf einzelner Ebene, ähnlich wie ein-Zeiger. Qualifizierte Komponenten werden hauptsächlich verwendet, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren. Wenn Sie z. b. 30 Komponenten in der [Component-Tabelle](component-table.md) aufgelistet haben, bei denen es sich um dieselbe Microsoft Word-Faxvorlage handelt, die in 30 Sprachen lokalisiert ist, können Sie diese mithilfe der [PublishComponent-Tabelle](publishcomponent-table.md)in eine Kategorie qualifizierter Komponenten gruppieren.

Qualifizierte Komponenten werden in der Komponenten Tabelle auf die gleiche Weise wie normale Komponenten eingegeben. Für jede Komponente müssen in der Component-Tabelle eine eindeutige GUID für die Komponenten-ID und der Komponenten Bezeichner angegeben werden. Außerdem werden qualifizierten Komponenten eine Kategorie-GUID und ein Textzeichen folgen Qualifizierer in der PublishComponent-Tabelle zugeordnet. Auf qualifizierte Komponenten wird durch die Kategorie-GUID und den Qualifizierer verwiesen, der nur auf die normale Komponente in der Komponenten Tabelle verweist.

Beispielsweise kann eine qualifizierte Komponenten-ID-GUID auf verschiedene Sprachversionen einer Ressourcen-DLL verweisen. In diesem Fall besteht die Gruppe der lokalisierten Ressourcen-DLLs aus der Kategorie, und die Zeichen folgen für numerische Gebiets Schema Bezeichner (LCID) werden häufig als Qualifizierer verwendet. Ein Entwickler könnte ein Installationspaket erstellen, das diese qualifizierten Komponenten für folgende Zwecke verwendet:

-   Suchen Sie den Pfad zu einer bestimmten Sprachversion der Ressourcen-DLL mithilfe von [**msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) oder [**msiprovidequalifiedcomponestex**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) , und installieren Sie die Ressource.
-   Bestimmen Sie alle Sprachversionen der Ressourcen-DLL, die durch Aufrufen von " [**msienumschlag componentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)" vorhanden sind.
-   Bereiten Sie die Anwendung für die Unterstützung zusätzlicher Sprachen vor. Ein zukünftiges Sprachpaket für die Anwendung kann die qualifizierte Komponente verwenden, um weitere Sprachversionen der Ressourcen-DLL hinzuzufügen.

Weitere Informationen finden Sie unter [using Qualified Components](using-qualified-components.md).

 

 



