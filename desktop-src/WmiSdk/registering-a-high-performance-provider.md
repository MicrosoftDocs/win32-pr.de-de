---
description: Wie andere Instanzanbieter registrieren Sie einen Hochleistungs Anbieter bei Microsoft Windows&\# 160; Verwaltungs Instrumentation (WMI), indem eine Instanz der \_ \_ Win32Provider-Klasse und der \_ \_ instanceproviderregistration-Klasse erstellt wird.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrieren eines High-Performance Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042003"
---
# <a name="registering-a-high-performance-provider"></a>Registrieren eines High-Performance Anbieters

Wie andere Instanzanbieter registrieren Sie einen Hochleistungs Anbieter bei Microsoft Windows-Verwaltungsinstrumentation (WMI), indem Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse und der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse erstellen. Die **\_ \_ Win32Provider** -Instanz definiert die physische Implementierung des Anbieters, und die **\_ \_ instanceproviderregistration** -Instanz definiert die Funktionsgruppe des Anbieters. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).

Im folgenden Verfahren wird beschrieben, wie ein Anbieter für Hochleistungs Instanzen registriert wird.

**So registrieren Sie einen Anbieter für Hochleistungs Instanzen**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.

    Stellen Sie sicher, dass Sie der [**\_ \_ Win32Provider**](--win32provider.md) -Instanz eine **clientloadableclsid** -Eigenschaft hinzufügen. Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter Prozess in-Process auf den Client, wobei **clientloadableclsid** als Klassen Bezeichner verwendet wird. Wenn sich der Anbieter und der Client auf unterschiedlichen Computern befinden, wird der Anbieter von WMI in-Process in den WMI-Prozess geladen. WMI verwendet auch **clientloadableclsid** , um Aktualisierungs Vorgänge zu unterstützen.

2.  Erstellen Sie eine Instanz der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](dynamic-qualifier.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren. Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll. Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.

    Ein Hochleistungs Anbieter muss auch die Unterstützung für Vorgänge, Enumerationsvorgänge oder beides angeben. Stellen Sie sicher, dass Sie die Eigenschaften " **supportsget** " und " **supportsenumeration** " in der Implementierung verwenden.

Im folgenden Codebeispiel wird gezeigt, wie Sie die [**\_ \_ Win32Provider**](--win32provider.md) -und [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klassen für einen Hochleistungs Anbieter implementieren.

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



