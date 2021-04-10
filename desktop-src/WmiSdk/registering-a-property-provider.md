---
description: Zum Erstellen eines WMI-Eigenschaften Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ propertyproviderregistration registrieren.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrieren eines Eigenschaften Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215341"
---
# <a name="registering-a-property-provider"></a>Registrieren eines Eigenschaften Anbieters

Zum Erstellen eines WMI- [*Eigenschaften Anbieters*](gloss-p.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md)registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie ein Eigenschaften Anbieter registriert wird.

**So registrieren Sie einen Eigenschaften Anbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Eigenschaften Anbieter beschreibt.

    Die [**\_ \_ Win32Provider**](--win32provider.md) -Klasse akzeptiert die Standardwerte für andere Eigenschaften, z. b. den **true** -Wert für die **Pure** -Eigenschaft. Weitere Informationen finden Sie unter [**\_ \_ Win32Provider**](--win32provider.md).

2.  Erstellen Sie eine Instanz der [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Die [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md) -Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse, die boolesche Werte bereitstellt, die Unterstützung für bestimmte Funktionen und ein Array von Zeichen folgen zur Angabe der Abfrage Unterstützung angeben.

    Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](dynamic-qualifier.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren. Der **dynamische** Qualifizierer signalisiert, dass WMI einen dynamischen Anbieter verwenden sollte, um die Klassen Instanzen abzurufen, die die unterstützten Eigenschaften enthalten. Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.

WMI ruft NewQuery für einen Ereignis Anbieter auf, wenn ein Client Consumer eine Ereignis Filter Abfrage registriert, die Verweise auf Ereignisse enthält, die von diesem Ereignis Anbieter unterstützt werden. Daher kann der Ereignis Anbieter, der für Instanzen Änderungs Ereignisse für die emailclass-Klasse verantwortlich ist, so eingerichtet werden, dass nur Benachrichtigungen für den Absender generiert werden. Wenn der Anbieter eine Abfrage empfängt, die eine Benachrichtigung über Änderungen an der Eigenschaft "Subject" anfordert, kann der Anbieter damit beginnen, diese Benachrichtigungen zu erstellen. In diesem Szenario ist es nicht erforderlich, dass WMI die Benachrichtigungen verwerfen, die nur vom Empfänger des Empfängers geändert werden.

Im folgenden MOF-Codebeispiel werden-Instanzen beschrieben, die verwendet werden können, um einen Eigenschaften Anbieter zu registrieren.

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
> Nur Administratoren können einen Eigenschaften Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md)erstellen.

 

 

 



