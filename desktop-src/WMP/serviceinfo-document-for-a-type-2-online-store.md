---
title: ServiceInfo-Dokument für eine Online-Store
description: ServiceInfo-Dokument für eine Online-Store
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player,ServiceInfo-Dokument
- Onlineshops,ServiceInfo-Dokument
- Typ 2 Onlineshops,ServiceInfo-Dokument
- ServiceInfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6830b4c54b037f254adb21624ed893ec16fa9b3973dfe1536170dff1b4f9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995430"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>ServiceInfo-Dokument für eine Online-Store

Anbieter von Onlineshops vom Typ 2 müssen Microsoft die URL eines XML-Dokuments bereitstellen, das den Onlineshop beschreibt. Windows Media Player 10 und Windows Media Player 11 verwenden Sie dieses Dokument, um zu bestimmen, wie die Benutzeroberfläche zum Hosten des Onlineshops konfiguriert wird.

In Windows Media Player 10 enthält das ServiceInfo-Dokument Folgendes:

-   Informationen zum Konfigurieren der Aufgabenbereiche, die Windows Media Player, wenn der Onlineshop aktiv ist. Ein Onlineshop kann einen, zwei oder drei Aufgabenbereiche haben.
-   Informationen, die zum Konfigurieren der Aufgabenbereichschaltflächen verwendet werden, z. B. der Schaltflächentext, die Schaltflächenfarbe und Tooltipps für die Schaltflächen.
-   URLs für Bilder, die Windows Media Player werden, um den Onlineshop zu identifizieren.
-   URLs von Webseiten, die vom Onlineshop bereitgestellt werden und Windows Media Player hosten.
-   Informationen dazu, Windows Media Player Setup den ersten Onlineshop konfigurieren soll, der dem Benutzer angezeigt wird.

In Windows Media Player 11 bietet das ServiceInfo-Dokument Folgendes:

-   Informationen, die zum Konfigurieren der Schaltfläche für die Registerkarte Onlineshops verwendet werden, z. B. der Schaltflächentext und die Tipps für die Schaltfläche.
-   URLs für Bilder, die Windows Media Player werden, um den Onlineshop zu identifizieren.
-   URLs von Webseiten, die vom Onlineshop bereitgestellt werden und Windows Media Player hosten.

Wenn Sie mit der Entwicklung Ihres Onlineshops beginnen, müssen Sie Microsoft die URL zu Ihrem ServiceInfo-Dokument bereitstellen. Während der Entwicklungsphase wird Ihr Onlineshop nur dann in Windows Media Player, wenn ein spezieller Registrierungsschlüssel festgelegt ist.

Nach der Veröffentlichung Ihres Onlineshops besteht das szenario der Benutzer, Windows Media Player ServiceInfo-Dokument automatisch aus dem Web abruft. In einigen Fällen ruft Windows Media Player ServiceInfo-Dokument jedoch vom Computer des Benutzers ab. Weitere Informationen finden Sie unter [Setting the Initial Online Store](setting-the-initial-online-store.md).

Wenn Windows Media Player ServiceInfo-Dokument aus dem Web abruft, wird eine Abfragezeichenfolge an die URL angefügt. Die Abfragezeichenfolge enthält Parameter, die Informationen über das Benutzer-Locale und die Windows Media Player bereitstellen.

Sie können statische oder dynamische ServiceInfo-Dokumente erstellen. Ein statisches ServiceInfo-Dokument verfügt über .xml Dateinamenerweiterung. Ein dynamisches ServiceInfo-Dokument ist eine ASP-Seite mit der Dateierweiterung ASP oder ASPX.

Nicht alle Elemente, die im ServiceInfo-Dokument zur Verfügung stehen, können von jedem Onlineshop verwendet werden, und einige Elemente sind für alle Onlineshops optional. Informationen zu den Typen von Onlineshops, die Sie erstellen können, und den für jeden Typ verfügbaren Features finden Sie [unter Windows Media Player Online Stores](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Dynamisches Erstellen des ServiceInfo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




