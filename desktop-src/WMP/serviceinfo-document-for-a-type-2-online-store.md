---
title: ServiceInfo-Dokument für einen Typ 2-Online Store
description: ServiceInfo-Dokument für einen Typ 2-Online Store
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037107"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>ServiceInfo-Dokument für einen Typ 2-Online Store

Typ 2 Online Store-Anbieter müssen Microsoft die URL eines XML-Dokuments bereitstellen, das den Online Shop beschreibt. Windows Media Player 10 und Windows Media Player 11 verwenden Sie dieses Dokument, um zu bestimmen, wie die Benutzeroberfläche zum Hosten des Online Stores konfiguriert wird.

In Windows Media Player 10 bietet das servicinput Info-Dokument Folgendes:

-   Informationen zum Konfigurieren der Aufgabenbereiche, die von Windows Media Player angezeigt werden, wenn der Online Store aktiv ist. Ein Online Store kann über einen, zwei oder drei Aufgabenbereiche verfügen.
-   Informationen, die zum Konfigurieren der Aufgabenbereichs Schaltflächen verwendet werden, z. b. der Schaltflächen Text, die Schaltflächen Farbe und Quick Infos für die Schaltflächen.
-   URLs für Images, die von Windows Media Player angezeigt werden, um den Online Store zu identifizieren.
-   URLs von Webseiten, die vom Online Store bereitgestellt werden, die von Windows Media Player in der Benutzeroberfläche gehostet werden.
-   Informationen dazu, wie das Windows Media Player-Setup den ersten Online Store konfigurieren soll, den der Benutzer sieht.

In Windows Media Player 11 bietet das servicinput Info-Dokument Folgendes:

-   Informationen, die verwendet werden, um die Schaltfläche für die Registerkarte "Online Stores" zu konfigurieren, z. b. den Schaltflächen Text und die QuickInfo
-   URLs für Images, die von Windows Media Player angezeigt werden, um den Online Store zu identifizieren.
-   URLs von Webseiten, die vom Online Store bereitgestellt werden, die von Windows Media Player in der Benutzeroberfläche gehostet werden.

Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, müssen Sie Microsoft die URL Ihres serviceInfo-Dokuments bereitstellen. Während der Entwicklungsphase wird der Online Shop in Windows Media Player nur angezeigt, wenn ein spezieller Registrierungsschlüssel festgelegt ist.

Nach der Veröffentlichung des Online Stores ist das Szenario, in dem Windows Media Player das serviceInfo-Dokument automatisch aus dem Internet abruft. In einigen Fällen ruft Windows Media Player jedoch das serviceInfo-Dokument vom Computer des Benutzers ab. Weitere Informationen finden Sie unter [Festlegen des ersten Online Stores](setting-the-initial-online-store.md).

Wenn Windows Media Player das servicanfo-Dokument aus dem Web abruft, fügt es eine Abfrage Zeichenfolge an die URL an. Die Abfrage Zeichenfolge enthält Parameter, die Informationen über das Gebiets Schema des Benutzers und die Windows-Media Player Version bereitstellen.

Sie können statische oder dynamische serviceingefo-Dokumente erstellen. Ein statisches serviceInfo-Dokument verfügt über die Dateinamenerweiterung. Xml. Ein dynamisches serviceInfo-Dokument ist eine ASP-Seite mit der Dateinamenerweiterung ". asp" oder ". aspx".

Nicht alle Elemente, die für die Verwendung im serviceInfo-Dokument verfügbar sind, können von jedem Online Store verwendet werden, und einige Elemente sind für alle Online Stores optional. Informationen zu den von Ihnen erstellten online speichern und den verfügbaren Funktionen für die einzelnen Typen finden Sie unter [Windows Media Player Online Stores](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 2 Online Stores**](about-type-2-online-stores.md)
</dt> <dt>

[**Dynamisches Erstellen des serviceingefo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




