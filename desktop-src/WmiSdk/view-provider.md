---
description: Der Ansichts Anbieter ist eine Instanz und ein Methoden Anbieter, die neue Klassen auf der Grundlage von Instanzen von anderen Klassen erstellt.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Ansichtsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866863"
---
# <a name="view-provider"></a>Ansichtsanbieter

Der Ansichts Anbieter ist eine Instanz und ein Methoden Anbieter, die neue Klassen auf der Grundlage von Instanzen von anderen Klassen erstellt. Sie können den Ansichts Anbieter verwenden, um Eigenschaften aus verschiedenen Quell Klassen, anderen Namespaces oder anderen Computern zu übernehmen und die Eigenschaften als einzelne Klasse zu kombinieren.

Als Instanzen-und Methoden Anbieter unterstützt der Ansichts Anbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle und die folgenden [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden:

-   [**"Kreateingestanceenumasync"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Weitere Informationen zu den Qualifizierern, mit denen Sie Ansichts Anbieter Klassen definieren, finden [Sie unter Qualifizierer für den Ansichts Anbieter](qualifiers-specific-to-the-view-provider.md).

Weitere Informationen zu Ansichten finden Sie unter [Verknüpfen von Klassen](linking-classes-together.md).

Zwei Versionen des Ansichts Anbieters sind auf 64-Bit-Plattformen verfügbar. Weitere Informationen finden Sie unter " [erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)".

Der Ansichts Anbieter wird in ViewProv.dll implementiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 



