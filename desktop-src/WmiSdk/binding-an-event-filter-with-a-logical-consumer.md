---
description: Nachdem Sie den logischen Ereignisconsumer und den Ereignis Filter erstellt haben, müssen Sie diese verknüpfen, wodurch der logische Consumer registriert wird, um Benachrichtigungen zu den vom Filter angegebenen Ereignissen zu erhalten.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Binden eines Ereignis Filters mit einem logischen Consumer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867788"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>Binden eines Ereignis Filters mit einem logischen Consumer

Nachdem Sie den logischen Ereignisconsumer und den Ereignis Filter erstellt haben, müssen Sie diese verknüpfen, wodurch der logische Consumer registriert wird, um Benachrichtigungen zu den vom Filter angegebenen Ereignissen zu erhalten.

Im folgenden Verfahren wird beschrieben, wie ein Ereignis Filter an einen logischen Consumer gebunden wird.

**So binden Sie einen Ereignis Filter mit einem logischen Consumer**

1.  Erstellen Sie eine Instanz der [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -System Klasse im WMI-Repository.

    Die [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Klasse ist eine Association-Klasse, die die Ereignis Filter Instanz und die logische consumerinstanz über  die Filter **-und** consumerverweiseigenschaften verknüpft. Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).

2.  Legen Sie die **Filter** -Eigenschaft auf die Instanz des Filters fest.
3.  Legen Sie die Eigenschaft **Consumer** auf die Instanz des logischen Consumers fest.
4.  Legen Sie die Eigenschaft **deliversynchron** fest, um den gewünschten Typ der Übermittlung zu bestimmen.

    Die **deliversynchron** -Eigenschaft bestimmt, wann WMI Ereignis Benachrichtigungen synchron oder asynchron bereitstellt. Wenn Sie diese Eigenschaft auf **true** festlegen, wird eine synchrone Übermittlung angefordert. Verwenden Sie die synchrone Übermittlung nur dann, wenn der permanente Consumer Ereignisse innerhalb von ungefähr 100 Mikrosekunden verarbeiten kann.

    > [!Note]  
    > Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

     

5.  Stellen Sie beim Aufheben der Registrierung des logischen Ereignisconsumers sicher, dass Sie die [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz löschen.

    Jede [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz stellt eine Registrierung für eine bestimmte Ereignis Benachrichtigung dar. Wenn Sie eine Bindung löschen, deaktiviert WMI die Registrierung. Möglicherweise müssen Sie die Instanzen des logischen Consumers und des Ereignis Filters löschen, um die Registrierung abhängig von der Implementierung zu deaktivieren.

Im folgenden Codebeispiel wird eine [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) -Instanz veranschaulicht, die eine Instanz einer [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse mit einem bestimmten Ereignis Filter verknüpft (die Instanz des Ereignisconsumers wurde im Thema [Erstellen eines logischen](creating-a-logical-consumer.md) Consumers erstellt, und der Ereignis Filter wurde im Thema [Erstellen eines Ereignis Filters](creating-an-event-filter.md) erstellt).

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Zwei Consumer, [**activescripteventconsumer**](activescripteventconsumer.md) und [**commandlineeventconsumer**](commandlineeventconsumer.md), funktionieren nur, wenn Ihr Ersteller Mitglied der lokalen Administratoren Gruppe ist.

**:** Wenn ein Administrator ein Abonnement erstellt, wird seine SID nicht für die Eigenschaft " **kreatorsid** " verwendet, sondern stattdessen die SID der lokalen Gruppe "Administratoren". Daher können Instanzen von verschiedenen Administratoren erstellt werden, und das Abonnement funktioniert weiterhin. Weitere Informationen finden Sie unter [sicheres empfangen von Ereignissen](receiving-events-securely.md).

Wenn ein Filter an einen logischen Consumer gebunden ist, wird das Ereignis von der [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) für Windows (ETW) aufgezeichnet. Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> </dl>

 

 
