---
description: Ein Klassenanbieter verwaltet eine Klasse oder eine Reihe von Klassen für WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Schreiben eines Klassenanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45815c795b6f43f3e7ec99b9ce9535c4d14b2bc8426ea5ca6b44f736415bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311939"
---
# <a name="writing-a-class-provider"></a>Schreiben eines Klassenanbieters

Ein Klassenanbieter verwaltet eine Klasse oder eine Reihe von Klassen für WMI. Ein Klassenanbieter kann entweder push oder pull sein. Das heißt, es kann entweder eigene Daten speichern oder WMI erlauben, Daten dafür im Windows-Verwaltungsdienst zu speichern. Obwohl ein Klassenanbieter auf einem bestimmten Computer installiert ist, kann er die Klassendefinitionen in einem gesamten Unternehmen ändern. Daher erstellen die meisten Entwickler nicht häufig Klassenanbieter.

Überprüfen Sie vor dem Erstellen eines Klassenanbieters, ob die unterstützten Klassen tatsächlich dynamisch generiert werden müssen. In den meisten Fällen ist die Liste der Klassen langsam veränderbar und endlich. In diesem Fall sollten Sie keinen Klassenanbieter erstellen müssen. Stattdessen können Sie Ihre Klassendefinitionen mithilfe der WMI-API oder einer MOF-Datei im WMI-Repository platzieren.

Im folgenden Verfahren wird beschrieben, wie ein Klassenanbieter implementiert wird.

**So implementieren Sie einen Klassenanbieter**

1.  Ermitteln Sie, ob ihr Anbieter ein Push- oder Pullanbieter ist.

    Ein Pullanbieter stellt Daten dynamisch als Reaktion auf eine Anwendungsanforderung bereit, während Pushanbieter ihre Daten einmal im WMI-Repository speichern. Weitere Informationen finden Sie unter [Bestimmen des Push- oder Pullstatus.](determining-push-or-pull-status.md)

2.  Entwerfen und registrieren Sie Ihren Klassenanbieter mit WMI.

    Klassenanbieter registrieren sich bei WMI, indem sie eine [**\_ \_ Win32Provider-Instanz**](--win32provider.md) und eine [**\_ \_ ClassProviderRegistration-Instanz**](--classproviderregistration.md) erstellen. Weitere Informationen finden Sie unter [Registrieren eines Klassenanbieters.](registering-a-class-provider.md)

3.  Implementieren Sie die [**IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für Ihren Anbieter.

    WMI verwendet [**IWbemProviderInit,**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) um einen Anbieter zu laden und zu initialisieren. Wenn Sie einen Pushanbieter entwerfen, ist **IWbemProviderInit** die einzige Schnittstelle, die Sie implementieren. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters.](initializing-a-provider.md)

    > [!Note]  
    > Klassenanbietern wird dringend empfohlen, das Multithreadmodell "Beide" zu verwenden.

     

4.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Beim Entwerfen Ihres Anbieters müssen Sie wahrscheinlich WMI-Schnittstellen aufrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter.](impersonating-a-client.md)

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsstufen für diesen Client zugreifen. Weitere Informationen finden Sie unter Annehmen der [Identität eines Clients.](impersonating-a-client.md)

5.  Implementieren Sie die [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) für Ihren Anbieter.

    Die [**IWbemServices-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ist die primäre Schnittstelle für einen Pullklassenanbieter. Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Klassenanbieter.](implementing-the-primary-interface-for-a-class-provider.md)

6.  Ersetzen Sie den bereits vorhandenen Anbieter durch Ihren neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie keinen bereits vorhandenen Anbieter zum Kopieren haben. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters.](updating-a-provider.md)

 

 



