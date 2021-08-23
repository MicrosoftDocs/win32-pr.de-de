---
description: Wie bei anderen Instanzanbietern registrieren Sie einen Hochleistungsanbieter bei Microsoft Windows&\# 160; Verwaltungsinstrumentation (Management Instrumentation, WMI) durch Erstellen einer Instanz der \_ \_ Klassen Win32Provider und \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrieren eines High-Performance Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ee52db95290810a046d23781dbccf666cd63a19b01bf9414b2e224b8137f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992570"
---
# <a name="registering-a-high-performance-provider"></a>Registrieren eines High-Performance Anbieters

Wie bei anderen Instanzanbietern registrieren Sie einen Hochleistungsanbieter bei der Microsoft Windows Management Instrumentation (WMI), indem Sie eine Instanz der [**\_ \_ Klassen Win32Provider**](--win32provider.md) und [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) erstellen. Die **\_ \_ Win32Provider-Instanz** definiert die physische Implementierung des Anbieters, und die **\_ \_ Instanz InstanceProviderRegistration** definiert den Featuresatz des Anbieters. Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)

Im folgenden Verfahren wird beschrieben, wie Sie einen Hochleistungsinstanzanbieter registrieren.

**So registrieren Sie einen Hochleistungsinstanzanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Anbieter beschreibt.

    Achten Sie darauf, der [**\_ \_ Win32Provider-Instanz**](--win32provider.md) eine **ClientLoadableCLSID-Eigenschaft** hinzuzufügen. Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter prozessin process mithilfe von **ClientLoadableCLSID** als Klassenbezeichner auf den Client. Wenn sich der Anbieter und der Client auf verschiedenen Computern befinden, lädt WMI den Anbieter in-Process in WMI. WMI verwendet auch **ClientLoadableCLSID,** um Aktualisierungsvorgänge zu unterstützen.

2.  Erstellen Sie eine Instanz der [**\_ \_ InstanceProviderRegistration-Klasse,**](--instanceproviderregistration.md) die den Funktionssatz des Anbieters beschreibt.

    Achten Sie darauf, die Klasse sowohl mit den Qualifizierern [**Dynamic als**](dynamic-qualifier.md) auch [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) zu kennzeichnen. Der **Dynamische Qualifizierer** signalisiert, dass WMI einen Anbieter verwenden soll, um die Klasseninstanzen abzurufen. Der  Anbieterqualifizierer gibt den Namen des Anbieters an, den WMI verwenden soll.

    Ein Hochleistungsanbieter muss auch Unterstützung für Vorgänge, Enumerationsvorgänge oder beides unterstützen. Stellen Sie sicher, dass Sie **die Eigenschaften SupportsGet** und **SupportsEnumeration** in Ihrer Implementierung verwenden.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie die [**\_ \_ Klassen Win32Provider**](--win32provider.md) und [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) für einen Hochleistungsanbieter implementieren.

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

[Erstellen eines Instanzanbieters zu einem High-Performance Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



