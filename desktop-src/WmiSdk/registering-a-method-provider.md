---
description: Zum Erstellen eines WMI-Methoden Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ methodproviderregistration registrieren.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrieren eines Methoden Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216891"
---
# <a name="registering-a-method-provider"></a>Registrieren eines Methoden Anbieters

Zum Erstellen eines WMI- [*Methoden Anbieters*](gloss-m.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ methodproviderregistration**](--methodproviderregistration.md)registrieren. Nachdem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md)erstellt haben, müssen Sie diesen Anbieter bei WMI registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie ein Methoden Anbieter registriert wird.

**So registrieren Sie einen Methoden Anbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.

    Die [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -System Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse. die einzige für einen Methoden Anbieter relevante Eigenschaft ist jedoch der Objekt Pfad zur [**\_ \_ Win32Provider**](--win32provider.md) -Instanz.

2.  Erstellen Sie eine Instanz der [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](dynamic-qualifier.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren. Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll. Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.

Im folgenden Codebeispiel wird beschrieben, wie ein Methoden Anbieter registriert wird.

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

 

 



