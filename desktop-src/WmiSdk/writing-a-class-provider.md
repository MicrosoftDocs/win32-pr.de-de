---
description: Ein Klassen Anbieter verwaltet eine Klasse oder eine Reihe von Klassen für WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Schreiben eines Klassen Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347410"
---
# <a name="writing-a-class-provider"></a>Schreiben eines Klassen Anbieters

Ein Klassen Anbieter verwaltet eine Klasse oder eine Reihe von Klassen für WMI. Ein Klassen Anbieter kann per Push oder Pull abgerufen werden. Das heißt, es kann entweder eigene Daten speichern oder WMI das Speichern von Daten im Windows-Verwaltungsdienst ermöglichen. Obwohl ein Klassen Anbieter auf einem bestimmten Computer installiert ist, kann er die Klassendefinitionen über ein gesamtes Unternehmen hinweg ändern. Daher erstellen die meisten Entwickler nicht häufig Klassen Anbieter.

Überprüfen Sie vor dem Erstellen eines Klassen Anbieters, ob die unterstützten Klassen wirklich dynamisch generiert werden müssen. In den meisten Fällen ist die Liste der Klassen langsam veränderlich und begrenzt. Wenn dies der Fall ist, sollten Sie keinen Klassen Anbieter erstellen müssen. Stattdessen können Sie Ihre Klassendefinitionen mithilfe der WMI-API oder einer MOF-Datei im WMI-Repository platzieren.

Im folgenden Verfahren wird beschrieben, wie ein Klassen Anbieter implementiert wird.

**So implementieren Sie einen Klassen Anbieter**

1.  Stellen Sie fest, ob es sich bei dem Anbieter um einen Push-oder Pull

    Ein Pull-Anbieter stellt Daten dynamisch als Reaktion auf eine Anwendungsanforderung bereit, während pushanbieter Ihre Daten im WMI-Repository einmal speichern. Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).

2.  Entwerfen und registrieren Sie den Klassen Anbieter bei WMI.

    Klassen Anbieter registrieren sich bei WMI, indem Sie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Instanz erstellen. Weitere Informationen finden Sie unter [Registrieren eines Klassen Anbieters](registering-a-class-provider.md).

3.  Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.

    WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren. Wenn Sie einen pushanbieter entwerfen, ist **iwbemproviderinit** die einzige Schnittstelle, die Sie implementieren werden. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).

    > [!Note]  
    > Klassen Anbietern wird dringend empfohlen, das Multithreading-Modell "both" zu verwenden.

     

4.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter](impersonating-a-client.md).

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

5.  Implementieren Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle für Ihren Anbieter.

    Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle ist die primäre Schnittstelle für einen Pull-Klassen Anbieter. Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Klassen Anbieter](implementing-the-primary-interface-for-a-class-provider.md).

6.  Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).

 

 



