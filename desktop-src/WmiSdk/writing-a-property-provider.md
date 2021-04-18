---
description: Ein Eigenschaften Anbieter ruft einzelne Eigenschaftswerte für Instanzen einer bestimmten Klasse ab, die im WMI-Repository gespeichert sind, und ändert Sie.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Schreiben eines Eigenschaften Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351724"
---
# <a name="writing-a-property-provider"></a>Schreiben eines Eigenschaften Anbieters

Ein Eigenschaften Anbieter ruft einzelne Eigenschaftswerte für Instanzen einer bestimmten Klasse ab, die im WMI-Repository gespeichert sind, und ändert Sie.

Im folgenden Verfahren wird beschrieben, wie ein Eigenschaften Anbieter erstellt wird.

**So erstellen Sie einen Eigenschaften Anbieter**

1.  Entwerfen und registrieren Sie Ihren Anbieter bei WMI.

    Instanzanbieter registrieren sich bei WMI, indem Sie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md) -Klasse erstellen. Weitere Informationen finden Sie unter [Registrieren eines Eigenschaften Anbieters](registering-a-property-provider.md).

2.  Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.

    WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren. Dies ist eine Aufgabe, die allen Anbietern gemeinsam ist. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).

    > [!Note]  
    > Eigenschafts Anbietern wird dringend empfohlen, das Multithreading-Modell "both" zu verwenden.

     

3.  Implementieren Sie die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Schnittstelle für Ihren Anbieter.

    Die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Schnittstelle ist die primäre Schnittstelle für einen Eigenschaften Anbieter. Die zwei Hauptmethoden sind [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) und [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty). Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Eigenschaften Anbieter](implementing-the-primary-interface-for-a-property-provider.md).

4.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter](impersonating-a-client.md).

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

5.  Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).

 

 



