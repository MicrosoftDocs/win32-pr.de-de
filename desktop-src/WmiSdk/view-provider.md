---
description: Der View-Anbieter ist ein Instanz- und Methodenanbieter, der neue Klassen basierend auf Instanzen anderer Klassen erstellt.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Ansichtsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec84f3a22a777da2212dcfe918f4294495ade54191cd4d37e17f2ac32c2f5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553262"
---
# <a name="view-provider"></a>Ansichtsanbieter

Der View-Anbieter ist ein Instanz- und Methodenanbieter, der neue Klassen basierend auf Instanzen anderer Klassen erstellt. Sie können den View-Anbieter verwenden, um Eigenschaften aus verschiedenen Quellklassen, unterschiedlichen Namespaces oder computern zu übernehmen und die Eigenschaften als einzelne Klasse zu kombinieren.

Als Instanz- und Methodenanbieter unterstützt der View-Anbieter die [**IWbemProviderInit-Standardschnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und die folgenden [**IWbemServices-Methoden:**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

-   [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Weitere Informationen zu den Qualifizierern, die zum Definieren von Ansichtsanbieterklassen verwendet werden, finden Sie unter [Qualifizierer, die für den Ansichtsanbieter spezifisch](qualifiers-specific-to-the-view-provider.md)sind.

Weitere Informationen zu Ansichten finden Sie unter [Verknüpfen von Klassen mit .](linking-classes-together.md)

Zwei Versionen des View-Anbieters sind auf 64-Bit-Plattformen verfügbar. Weitere Informationen finden Sie unter [Abrufen und Bereitstellen von Daten auf einem 64-Bit-Computer.](getting-and-providing-data-on-a-64-bit-computer.md)

Der Ansichtsanbieter wird in ViewProv.dll implementiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 



