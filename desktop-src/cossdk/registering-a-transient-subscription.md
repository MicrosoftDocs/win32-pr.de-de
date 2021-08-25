---
description: Vorübergehende Abonnements können nicht mit dem Verwaltungstool Komponentendienste festgelegt werden. Sie müssen die COM+-Verwaltungsschnittstellen verwenden, um ein vorübergehendes Abonnement zu erstellen oder zu aktualisieren.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrieren eines vorübergehenden Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f93b543a4602b0b4ed7ed4177133f3eb8f543a0db02750af8657ab36f310993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990440"
---
# <a name="registering-a-transient-subscription"></a>Registrieren eines vorübergehenden Abonnements

Vorübergehende Abonnements fordern ein Ereignis für ein bestimmtes Abonnentenobjekt an, das bereits vorhanden ist. Vorübergehende Abonnements werden im COM+-Katalog gespeichert, aber das Abonnement wird gelöscht, wenn das Ereignissystem oder Betriebssystem beendet wird. Im Gegensatz zu persistenten Abonnements sind vorübergehende Abonnements an ein bestimmtes Objekt gebunden und werden nur im Ereignissystem gespeichert. Wenn ein Problem mit dem Ereignissystem oder Betriebssystem vorliegt, wird das Abonnement nicht mehr angezeigt. Vorübergehende Abonnements können effizienter sein als persistente Abonnements, aber Sie müssen deren Objektlebenszyklen verwalten.

Vorübergehende Abonnements können nicht mit dem Verwaltungstool Komponentendienste festgelegt werden. Sie müssen die COM+-Verwaltungsschnittstellen verwenden, um ein vorübergehendes Abonnement zu erstellen oder zu aktualisieren.

## <a name="visual-basic"></a>Visual Basic

Im folgenden Verfahren wird beschrieben, wie Sie mit microsoft Visual Basic ein vorübergehendes Abonnement erstellen:

1.  Geben Sie ein Abonnement als vorübergehend an, indem Sie der [**Sammlung TransientSubscriptions**](transientsubscriptions.md) einen neuen Eintrag hinzufügen und die SubscriberInterface-Eigenschaft auf die [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) des Abonnentenobjekts festlegen. COM+-Ereignisse erstellt beim Auslösen eines Ereignisses keine neue Instanz des Abonnentenobjekts, sondern verwendet stattdessen die angegebene Instanz. COM+-Ereignisse enthält einen Verweiszähler für das Abonnentenobjekt, bis das Abonnement aus dem System entfernt wird.
2.  Erstellen Sie eine COM+-Serveranwendung (eine .exe, eine .dll oder eine OCX-Datei) mit einem -Objekt, das die Schnittstellen oder Methoden implementiert, die Sie abonnieren möchten.
3.  Erstellen Sie Ihr vorübergehendes Abonnement mit dem folgenden Code, indem Sie die CLSID des [Ereignisklassenobjekts](the-com--event-class-object.md) und die Instanz des Abonnentenobjekts übergeben. Mit dem Verwaltungstool Komponentendienste können Sie die EventCLSID-Eigenschaft abrufen, indem Sie mit der rechten Maustaste auf die COM+-Komponente klicken, **Eigenschaften** auswählen und die Registerkarte **Allgemein** auswählen.

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

Im folgenden Beispiel wird veranschaulicht, wie die CreateTransientSubscription-Funktion aufgerufen wird, um eine Schnittstelle namens IStockTbestand zu abonnieren, die über eine Methode namens UpdateStock verfügt.

1.  Erstellen Sie eine Ereignisklasse, die die Schnittstelle IStockT untereinander unterstützt, die über die Methode UpdateStock verfügt.
2.  Fügen Sie in Ihrem Abonnentenprojekt eine Klasse hinzu, die die IStockTzier-Schnittstelle implementiert.
3.  Wenn Sie abonnieren möchten, führen Sie den folgenden Code aus:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

Die CreateTransientSubscription-Funktion gibt eine Zeichenfolge zurück, bei der es sich um eine GUID handelt, die als Handle oder Cookie zum späteren Widerrufen des Abonnements verwendet werden kann. Um das Abonnement zu entfernen, rufen Sie die [**Remove-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) von [**COMAdminCatalogCollection**](comadmincatalogcollection.md) für die [**TransientSubscriptions-Auflistung**](transientsubscriptions.md) auf und übergeben den Index, der dem Abonnement mit der zuvor empfangenen GUID entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren eines Abonnements](registering-a-subscription.md)
</dt> </dl>

 

 
