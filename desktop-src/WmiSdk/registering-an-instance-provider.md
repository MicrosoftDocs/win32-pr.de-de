---
description: Zum Erstellen eines WMI-Instanzanbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ instanceproviderregistration registrieren.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrieren eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528502"
---
# <a name="registering-an-instance-provider"></a>Registrieren eines Instanzanbieters

Zum Erstellen eines WMI- [*Instanzanbieters*](gloss-i.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md)registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie ein Instanzanbieter registriert wird.

**So registrieren Sie einen Instanzanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Die [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse, die boolesche Werte bereitstellt, die Unterstützung für bestimmte Funktionen und ein Array von Zeichen folgen zur Angabe der Abfrage Unterstützung angeben.

    Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](standard-wmi-qualifiers.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren. Der Qualifizierer signalisiert, dass WMI einen **dynamischen** Anbieter zum Abrufen der Klassen Instanzen verwenden soll. Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.

Im folgenden Codebeispiel wird beschrieben, wie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Instanz registriert werden.

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

 

 



