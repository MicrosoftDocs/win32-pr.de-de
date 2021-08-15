---
description: Ein Methodenanbieter ermöglicht den WMI-Zugriff auf die Methoden einer Klasse. Beispielsweise kann eine Klasse, die eine Anwendung darstellt, über eine Methode verfügen, die die Anwendung beendet.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Schreiben eines Methodenanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea5121d4a9438744ad62b666e62d4ffa90c39428020d3e39c80a6de26e295959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311929"
---
# <a name="writing-a-method-provider"></a>Schreiben eines Methodenanbieters

Ein Methodenanbieter ermöglicht den WMI-Zugriff auf die Methoden einer Klasse. Beispielsweise kann eine Klasse, die eine Anwendung darstellt, über eine Methode verfügen, die die Anwendung beendet.

Das Ändern der Reihenfolge von Methodeneingabe- und -ausgabeparametern beim Aktualisieren eines vorhandenen Methodenanbieters kann zu Fehlern bei Anwendungen führen, die die -Methode aufrufen. Die Reihenfolge der Eingabe- oder Ausgabeparameter wird [](standard-wmi-qualifiers.md) durch den Wert des ID-Qualifizierers für jeden Parameter festgelegt. Der erste Parameter hat den **ID-Wert** 0 (null). Fügen Sie neue Eingabeparameter am Ende der vorhandenen Parameter hinzu, anstatt sie in die bereits eingerichtete Sequenz einfügungen zu müssen.

Im folgenden Verfahren wird beschrieben, wie ein Methodenanbieter implementiert wird.

**So implementieren Sie einen Methodenanbieter**

1.  Entwerfen und registrieren Sie Ihren Klassenanbieter bei WMI.

    Klassenanbieter registrieren sich bei WMI, indem sie eine [**\_ \_ Win32Provider-Instanz**](--win32provider.md) und eine [**\_ \_ MethodProviderRegistration-Klasse**](--methodproviderregistration.md) erstellen. Weitere Informationen finden Sie unter [Registrieren eines Methodenanbieters.](registering-a-method-provider.md)

2.  Implementieren Sie [**die IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für Ihren Anbieter.

    > [!Note]  
    > Methodenanbietern wird dringend empfohlen, das Multithreadingmodell "Both" zu verwenden.

     

3.  Implementieren Sie [**die IWbemServices::ExecMethodAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) für Ihren Anbieter.

    Die [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ist die primäre Schnittstelle für einen Methodenanbieter. Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Methodenanbieter.](implementing-the-primary-interface-for-a-method-provider.md)

4.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Beim Entwerfen Ihres Anbieters müssen Sie wahrscheinlich WMI-Schnittstellen aufrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode und](calling-a-method.md) Verwalten von [Sicherheitsebenen in einem Anbieter.](impersonating-a-client.md)

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter [Impersonating a Client](impersonating-a-client.md).

5.  Ersetzen Sie den bereits vorhandene Anbieter durch Ihren neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen bereits vorhandene Anbieter zum Kopieren verfügen. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters.](updating-a-provider.md)

 

 



