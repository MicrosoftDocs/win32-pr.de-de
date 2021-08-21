---
description: Zum Erstellen eines WMI-Methodenanbieters müssen Sie die \_ \_ Win32Provider-Instanz registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von \_ \_ MethodProviderRegistration verwenden.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrieren eines Methodenanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a85fb93a30f6a996dd8e7255cc53f7a58a7fe37df35eb16bdca8de038e8704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992560"
---
# <a name="registering-a-method-provider"></a>Registrieren eines Methodenanbieters

Zum Erstellen eines [*WMI-Methodenanbieters*](gloss-m.md) müssen Sie die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md)verwenden. Nachdem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md)erstellt haben, müssen Sie diesen Anbieter bei WMI registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie Sie einen Methodenanbieter registrieren.

**So registrieren Sie einen Methodenanbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Anbieter beschreibt.

    Die [**\_ \_ MethodProviderRegistration-Systemklasse**](--methodproviderregistration.md) erbt viele Eigenschaften von der übergeordneten [**\_ \_ ObjectProviderRegistration-Klasse.**](--objectproviderregistration.md) Die einzige für einen Methodenanbieter relevante Eigenschaft ist jedoch der Objektpfad zur [**\_ \_ Win32Provider-Instanz.**](--win32provider.md)

2.  Erstellen Sie eine Instanz der [**\_ \_ MethodProviderRegistration-Klasse,**](--methodproviderregistration.md) die den Featuresatz des Anbieters beschreibt.

    Achten Sie darauf, die -Klasse mit den [**Qualifizierern Dynamic**](dynamic-qualifier.md) und [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) zu kennzeichnen. Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter verwenden soll, um die Klasseninstanzen abzurufen. Der **Anbieterqualifizierer** gibt den Namen des Anbieters an, den WMI verwenden soll.

Im folgenden Codebeispiel wird beschrieben, wie ein Methodenanbieter registriert wird.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



