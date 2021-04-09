---
description: Vorübergehende Abonnements können nicht mithilfe des Verwaltungs Tools für Komponenten Dienste festgelegt werden. Sie müssen die com+-Verwaltungs Schnittstellen verwenden, um ein vorübergehendes Abonnement zu erstellen oder zu aktualisieren.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrieren eines vorübergehenden Abonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126704"
---
# <a name="registering-a-transient-subscription"></a>Registrieren eines vorübergehenden Abonnements

Vorübergehende Abonnements fordern ein Ereignis für ein bestimmtes Abonnenten Objekt an, das bereits vorhanden ist. Vorübergehende Abonnements werden im com+-Katalog gespeichert, aber das Abonnement wird gelöscht, wenn das Ereignis System oder das Betriebssystem beendet wird. Im Gegensatz zu permanenten Abonnements sind vorübergehende Abonnements an ein bestimmtes Objekt gebunden und nur im-Ereignis System gespeichert. Wenn ein Problem mit dem Ereignis System oder dem Betriebssystem vorliegt, verschwindet das Abonnement. Vorübergehende Abonnements können effizienter als persistente Abonnements sein, aber Sie müssen deren Objekt Lebenszyklen verwalten.

Vorübergehende Abonnements können nicht mithilfe des Verwaltungs Tools für Komponenten Dienste festgelegt werden. Sie müssen die com+-Verwaltungs Schnittstellen verwenden, um ein vorübergehendes Abonnement zu erstellen oder zu aktualisieren.

## <a name="visual-basic"></a>Visual Basic

Im folgenden Verfahren wird das Erstellen eines vorübergehenden Abonnements mit Microsoft Visual Basic beschrieben:

1.  Geben Sie ein Abonnement als flüchtig an, indem Sie einen neuen Eintrag zur [**transientabonnements**](transientsubscriptions.md) -Auflistung hinzufügen und die Eigenschaft "Abonnement Schnittstelle" auf die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Abonnenten Objekts festlegen. Com+-Ereignisse erstellt keine neue Instanz des Abonnenten Objekts, wenn ein Ereignis ausgelöst wird, sondern verwendet stattdessen die von Ihnen angegebene Instanz. Com+-Ereignisse enthalten einen Verweis Zähler für das Abonnenten Objekt, bis das Abonnement aus dem System entfernt wird.
2.  Erstellen Sie eine COM+-Serveranwendung (eine exe-, dll-oder OCX-Datei) mit einem Objekt, das die Schnittstellen oder Methoden implementiert, die Sie abonnieren möchten.
3.  Erstellen Sie mit dem folgenden Code ein vorübergehendes Abonnement, indem Sie die CLSID des [Ereignis Klassen](the-com--event-class-object.md) Objekts und die Instanz des Abonnenten Objekts übergeben. Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie die eventclsid-Eigenschaft erhalten, indem Sie mit der rechten Maustaste auf die COM+-Komponente klicken, **Eigenschaften** auswählen und die Registerkarte **Allgemein** auswählen.

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

Das folgende Beispiel veranschaulicht, wie die Funktion "foratetransientabonnement" aufgerufen wird, um eine Schnittstelle mit dem Namen "istockticker" zu abonnieren, die eine Methode namens "updatestock" aufweist.

1.  Erstellen Sie eine Ereignisklasse, die die istockticker-Schnittstelle unterstützt, die über eine Methode, updatestock verfügt.
2.  Fügen Sie in Ihrem Abonnenten Projekt eine Klasse hinzu, die die istockticker-Schnittstelle implementiert.
3.  Wenn Sie abonnieren möchten, führen Sie den folgenden Code aus:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

Die Funktion "kreatetransientabonnementabonnement" gibt eine Zeichenfolge zurück, die eine GUID ist, die als handle oder Cookie verwendet werden kann, um das Abonnement später aufzuheben. Um das Abonnement zu entfernen, rufen Sie die [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode von [**comadmincatalogcollection**](comadmincatalogcollection.md) für die [**transientabonnements**](transientsubscriptions.md) -Auflistung auf, und übergeben Sie den Index, der dem Abonnement mit der zuvor empfangenen GUID entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren eines Abonnements](registering-a-subscription.md)
</dt> </dl>

 

 
