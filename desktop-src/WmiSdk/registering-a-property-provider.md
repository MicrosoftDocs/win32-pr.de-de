---
description: Um einen WMI-Eigenschaftenanbieter zu erstellen, müssen Sie die Win32Provider-Instanz registrieren, die Ihren Anbieter mithilfe einer Instanz von \_ \_ \_ \_ PropertyProviderRegistration darstellt.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrieren eines Eigenschaftenanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbbec33f81fdfa9c1d32b20f2f5cff44566c417b1311c3429bbfaa400b68625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554208"
---
# <a name="registering-a-property-provider"></a>Registrieren eines Eigenschaftenanbieters

Um einen WMI-Eigenschaftenanbieter [*zu erstellen,*](gloss-p.md) müssen Sie die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von [**\_ \_ PropertyProviderRegistration verwenden.**](--propertyproviderregistration.md) Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Beim folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters beschrieben.](registering-a-provider.md)

Im folgenden Verfahren wird beschrieben, wie Sie einen Eigenschaftenanbieter registrieren.

**So registrieren Sie einen Eigenschaftenanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Eigenschaftenanbieter beschreibt.

    Die [**\_ \_ Win32Provider-Klasse**](--win32provider.md) akzeptiert die Standardwerte für andere Eigenschaften, z. B. den **TRUE-Wert** für die **Pure-Eigenschaft.** Weitere Informationen finden Sie unter [**\_ \_ Win32Provider**](--win32provider.md).

2.  Erstellen Sie eine Instanz der [**\_ \_ PropertyProviderRegistration-Klasse,**](--propertyproviderregistration.md) die den Funktionssatz des Anbieters beschreibt.

    Die [**\_ \_ PropertyProviderRegistration-Klasse**](--propertyproviderregistration.md) erbt viele Eigenschaften von der übergeordneten [**\_ \_ ObjectProviderRegistration-Klasse,**](--objectproviderregistration.md) die boolesche Werte zur Unterstützung bestimmter Features und ein Array von Zeichenfolgen zur Angabe der Abfrageunterstützung enthält.

    Achten Sie darauf, die Klasse sowohl mit den Qualifizierern [**Dynamic als**](dynamic-qualifier.md) auch [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) zu kennzeichnen. Der **Dynamische** Qualifizierer signalisiert, dass WMI einen dynamischen Anbieter verwenden soll, um die Klasseninstanzen abzurufen, die die unterstützten Eigenschaften enthalten. Der  Anbieterqualifizierer gibt den Namen des Anbieters an, den WMI verwenden soll.

WMI ruft NewQuery für einen Ereignisanbieter auf, wenn ein Clientverbraucher eine Ereignisfilterabfrage registriert, die Verweise auf Ereignisse enthält, die von diesem Ereignisanbieter unterstützt werden. Daher kann der Ereignisanbieter, der für Instanzänderungsereignisse für die EmailClass-Klasse verantwortlich ist, so eingerichtet werden, dass nur Benachrichtigungen für den Absender generiert werden. Wenn der Anbieter eine Abfrage empfängt, die eine Benachrichtigung über Änderungen an der subject-Eigenschaft anfragt, kann der Anbieter mit der Generierung dieser Benachrichtigungen beginnen. In diesem Szenario ist WMI nicht erforderlich, um die Benachrichtigungen zu verwerfen, die nur Empfängeränderungen melden.

Im folgenden MOF-Codebeispiel werden Instanzen beschrieben, die zum Registrieren eines Eigenschaftenanbieters verwendet werden können.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> Nur Administratoren können einen Eigenschaftenanbieter registrieren oder löschen, indem sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ PropertyProviderRegistration erstellen.**](--propertyproviderregistration.md)

 

 

 



