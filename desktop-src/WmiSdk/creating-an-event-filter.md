---
description: Ein Ereignis Filter ist eine WMI-Klasse, die beschreibt, welche Ereignisse WMI an einen physischen Consumer übergibt.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Erstellen eines Ereignis Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351137"
---
# <a name="creating-an-event-filter"></a>Erstellen eines Ereignis Filters

Ein Ereignis Filter ist eine WMI-Klasse, die beschreibt, welche Ereignisse WMI an einen physischen Consumer übergibt. Beispielsweise kann ein Ereignis Filter WMI anweisen, alle Energie Verwaltungs Ereignisse oder alle Systemneustart Ereignisse an einen Consumer zu übermitteln. Ein Ereignis Filter beschreibt auch die Bedingungen, unter denen WMI die Ereignisse übermittelt. Ein Ereignis Filter kann ein System internes oder ein extrinsisches Ereignis angeben. und der Filter kann auf Ereignisse verweisen, die aus dem-Namespace stammen, d. –. mit Ausnahme des Namespace des Filters. Der permanente Consumer muss in den Consumer-, Filter-und Binding-Instanzen die gleiche " [**kreatorsid**](--eventconsumer.md) " aufweisen. Weitere Informationen finden Sie unter [sicheres empfangen von Ereignissen](receiving-events-securely.md).

Im folgenden Verfahren wird beschrieben, wie ein Ereignis Filter erstellt wird.

**So erstellen Sie einen Ereignis Filter**

1.  Erstellen Sie eine Instanz der WMI- [**\_ \_ EventFilter**](--eventfilter.md) -System Klasse.
2.  Erstellen Sie einen eindeutigen Bezeichner für Ihren Filter mit der **Name** -Eigenschaft auf zwei Arten:

    -   Verwenden Sie ein privates Schema.

        Das willkürliche benennen ihrer Ereignis Filter funktioniert, solange Sie nicht mit anderen Filter Benennungs Schemas in Konflikt stehen. Benennungs Konflikte müssen vermieden werden, da das Hinzufügen einer Instanz mit einem doppelten **namens** Wert die alte Instanz überschreibt.

    -   Verwenden Sie einen Globally Unique Identifier (GUID).

        Wenn Sie den **Namen** leer lassen, füllt WMI den **Namen** mit einer GUID aus.

3.  Beschreiben Sie den Ereignistyp, den Sie mit der **Query** -Eigenschaft filtern möchten.

    Die **Query** -Eigenschaft enthält die WMI Query Language (WQL)-Abfrage, die den Typ des zu filternden Ereignisses beschreibt. Sie können mit einer Vielzahl von Operatoren und Erweiterungen von WQL eine exakte Filterung erzielen.

    Ein NT-Protokoll Ereignis wird generiert, wenn eine Abfrage von einem permanenten Ereignisconsumer fehlschlägt. Die Quelle des Ereignisses ist WinMgmt, die Ereignis-ID ist 10, und der Ereignistyp ist Fehler.

    WMI ist effizienter bei der Verarbeitung restriktiver, spezifischer Abfragen als bei umfangreichen Abfragen. Indem Sie eine bestimmte Abfrage erstellen, können Sie unnötige prozessübergreifende Kommunikation und Netzwerk Datenverkehr vermeiden. Bei Ereignissen, die von einem Anbieter generiert werden, führt WMI die Filterung im Prozess für den Anbieter durch. Dadurch wird sichergestellt, dass nur Ereignisse, die dem Filter entsprechen, die Kosten für die prozessübergreifende Kommunikation verursachen Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).

4.  Legen Sie die **QueryLanguage** -Eigenschaft auf den Typ der Abfragesprache fest, den Sie in der **Query** -Eigenschaft verwenden.

    Sie legen " **QueryLanguage** " fast immer auf "WQL" fest.

Im folgenden Codebeispiel wird ein Ereignis Filter beschrieben, der jedes Mal ein Ereignis signalisiert, wenn WMI eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse im root \\ CIMV2-Namespace erstellt.

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Die **eventnamespace** -Eigenschaft gibt den Namespace an, von dem die Ereignisse stammen. Sie müssen keine Instanz der Filter in dem Namespace erstellen, von dem die Ereignisse stammen. Wenn Sie den Namespace nicht angeben, erstellt WMI den Filter im Standard Namespace. Die systeminternen Ereignis Klassen, z. b. [**\_ \_ instanceoperationevent**](--instanceoperationevent.md) , sind in jedem Namespace verfügbar.

Um den logischen Consumer für Ereignis Benachrichtigungen zu registrieren, müssen Sie die Ereignis Filter an einen logischen Consumer binden. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).

 

 



