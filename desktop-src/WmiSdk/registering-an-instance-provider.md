---
description: Um einen WMI-Instanzanbieter zu erstellen, müssen Sie die Win32Provider-Instanz registrieren, die Ihren Anbieter darstellt, indem Sie eine \_ \_ Instanz von \_ \_ InstanceProviderRegistration verwenden.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrieren eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc97668a41327eabbeab43760703519fa9009c855c25cf77638459050bb5c71d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817078"
---
# <a name="registering-an-instance-provider"></a>Registrieren eines Instanzanbieters

Um einen WMI-Instanzanbieter [*zu erstellen,*](gloss-i.md) müssen Sie die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von [**\_ \_ InstanceProviderRegistration verwenden.**](--instanceproviderregistration.md) Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Beim folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters beschrieben.](registering-a-provider.md)

Im folgenden Verfahren wird beschrieben, wie Sie einen Instanzanbieter registrieren.

**So registrieren Sie einen Instanzanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ InstanceProviderRegistration-Klasse,**](--instanceproviderregistration.md) die den Funktionssatz des Anbieters beschreibt.

    Die [**\_ \_ InstanceProviderRegistration-Klasse**](--instanceproviderregistration.md) erbt viele Eigenschaften von der übergeordneten [**\_ \_ ObjectProviderRegistration-Klasse,**](--objectproviderregistration.md) die boolesche Werte zur Unterstützung bestimmter Features und ein Array von Zeichenfolgen zur Angabe der Abfrageunterstützung enthält.

    Achten Sie darauf, die Klasse sowohl mit den Qualifizierern [**Dynamic als**](standard-wmi-qualifiers.md) auch [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) zu kennzeichnen. Der Qualifizierer signalisiert, dass WMI einen dynamischen Anbieter **verwenden** soll, um die Klasseninstanzen abzurufen. Der  Anbieterqualifizierer gibt den Namen des Anbieters an, den WMI verwenden soll.

Im folgenden Codebeispiel wird beschrieben, wie Sie eine [**\_ \_ Win32Provider-**](--win32provider.md) und [**\_ \_ InstanceProviderRegistration-Instanz**](--instanceproviderregistration.md) registrieren.

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



