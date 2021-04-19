---
description: Ein Methoden Anbieter ermöglicht dem WMI-Zugriff auf die Methoden einer Klasse. Beispielsweise kann eine-Klasse, die eine Anwendung darstellt, über eine-Methode verfügen, die die Anwendung beendet.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Schreiben eines Methoden Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345270"
---
# <a name="writing-a-method-provider"></a>Schreiben eines Methoden Anbieters

Ein Methoden Anbieter ermöglicht dem WMI-Zugriff auf die Methoden einer Klasse. Beispielsweise kann eine-Klasse, die eine Anwendung darstellt, über eine-Methode verfügen, die die Anwendung beendet.

Das Ändern der Reihenfolge der Eingabe-und Ausgabeparameter der Methode beim Aktualisieren eines vorhandenen Methoden Anbieters kann zu Fehlern bei Anwendungen führen, die die-Methode aufruft. Die Reihenfolge der Eingabe-oder Ausgabeparameter wird durch den Wert des [**ID**](standard-wmi-qualifiers.md) -Qualifizierers für jeden Parameter festgelegt. Der erste Parameter hat den **ID** -Wert 0 (null). Fügen Sie am Ende der vorhandenen Parameter neue Eingabeparameter hinzu, anstatt Sie in die bereits festgelegte Sequenz einzufügen.

Im folgenden Verfahren wird beschrieben, wie ein Methoden Anbieter implementiert wird.

**So implementieren Sie einen Methoden Anbieter**

1.  Entwerfen und registrieren Sie den Klassen Anbieter bei WMI.

    Klassen Anbieter werden bei WMI registriert, indem eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -Klasse erstellt werden. Weitere Informationen finden Sie unter [Registrieren eines Methoden Anbieters](registering-a-method-provider.md).

2.  Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.

    > [!Note]  
    > Methoden Anbietern wird dringend empfohlen, das Multithreading-Modell "both" zu verwenden.

     

3.  Implementieren Sie die [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) -Methode für Ihren Anbieter.

    Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle ist die primäre Schnittstelle für einen Methoden Anbieter. Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Methoden Anbieter](implementing-the-primary-interface-for-a-method-provider.md).

4.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter](impersonating-a-client.md).

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

5.  Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).

 

 



