---
title: Zuletzt verwendete Elemente
description: Die Liste Zuletzt verwendete Elemente ist ein Bereich im Anwendungsmenü, in dem die zuletzt verwendeten Elemente (MRU) für eine Anwendung angezeigt werden.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1d67c38e1eb9014cfd3349881ed2849755ebc89489cc925052aa690f54adc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810880"
---
# <a name="recent-items"></a>Zuletzt verwendete Elemente

Die Liste Zuletzt verwendete Elemente ist ein Bereich im [Anwendungsmenü,](windowsribbon-controls-applicationmenu.md) in dem die zuletzt verwendeten Elemente (MRU) für eine Anwendung angezeigt werden.

-   [Details](#details)
-   [Eigenschaften zuletzt verwendeter Elemente](#recent-items-properties)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht eine Liste zuletzt verwendeter Elemente von WordPad für Windows 7).

![Screenshot der Liste der zuletzt erstellten Elemente im Microsoft-Farbband.](images/controls/recentitems.png)

Das [](windowsribbon-controls-applicationmenu.md) Anwendungsmenü kann über eine [**ApplicationMenu.RecentItems-Liste**](windowsribbon-element-applicationmenu-recentitems.md) verfügen, die durch ein **ApplicationMenu.RecentItems-Element** dargestellt wird, um aktuelle Dokumente, Bilder, Filme und andere Projekte anzuzeigen, an der ein Benutzer bereits arbeitet. Die Anzahl der aufgelisteten Elemente reicht von null bis zur maximalen Anzahl, die im Markup angegeben ist, mit einem Standardwert von zehn. Die letzten Elemente werden als nummerierte Liste von Zeichenfolgen angezeigt, die Dateinamen angeben. Es wird empfohlen, die [**Command.LabelDescription-Eigenschaft**](windowsribbon-element-command-labeldescription.md) zu verwenden, um den vollständigen Pfad für den Dateispeicherort zu geben, wie im folgenden Screenshot gezeigt.

![Screenshot einer Liste zuletzt verwendeter Elemente in einem Anwendungsmenü.](images/overviews/applicationmenu-menurecentitems.png)

Das [**RecentItems-Element**](windowsribbon-element-recentitems.md) verfügt über ein *EnablePinning-Attribut,* das, wenn es auf festgelegt ist, ein Stecknadelsymbol rechts neben jedem Element in der Liste anzeigt, wie im folgenden Screenshot `true` gezeigt.

> [!Note]  
> Das Anheften ist standardmäßig aktiviert, wenn das *EnablePinning-Attribut* nicht angegeben ist.

 

![Screenshot der zuletzt in einem Anwendungsmenü angeheften Elemente.](images/overviews/applicationmenu-menurecentitemspinned.png)

Der anheftende Algorithmus soll dazu dienen, dass Elemente nicht aus der Liste Zuletzt **verwendete Elemente fallen.** Der Algorithmus erzeugt das folgende Verhalten:

-   Ein neues Element wird immer oben in der Liste Letzte **Elemente** hinzugefügt.
-   Elemente werden im Laufe der Zeit in der Liste nach unten bewegt. Sobald die Liste voll ist (erreicht die maximale Anzahl von Elementen, die im Markup angegeben sind), fallen ältere Elemente vom unteren Rand der Liste ab, wenn neue Elemente am Anfang der Liste hinzugefügt werden.
-   Wenn ein Element bereits in der Liste angezeigt wird, aber erneut darauf zugegriffen wird, wird es wieder an den Anfang der Liste zurück bewegt.
-   Wenn ein Element angeheftet ist, wird es weiterhin in der Liste nach unten geschaltet, aber nicht vom unteren Rand. Wenn die Liste voll ist, fällt stattdessen das erste entpinnte Element oberhalb des angeheftet Elements aus, wenn der Liste ein neues Element hinzugefügt wird.
-   Wenn die Anzahl angehefteter Elemente jemals die maximale Anzahl von Elementen erreicht, werden der Liste keine neuen Elemente hinzugefügt, bis ein Element entpinnt ist.

## <a name="recent-items-properties"></a>Eigenschaften zuletzt verwendeter Elemente

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das Steuerelement Zuletzt verwendete Elemente.

In der Regel wird die Eigenschaft Zuletzt verwendete Elemente in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement Zuletzt verwendete Elemente zugeordnet sind.



| Eigenschaftsschlüssel                                                                       | Hinweise                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [\_ \_ PKEY-Keytip der Benutzeroberfläche](windowsribbon-reference-properties-uipkey-keytip.md)           | Kann nur durch Ungültigkeit aktualisiert werden. |
| [UI \_ PKEY \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md) | Kann nur durch Ungültigkeit aktualisiert werden. |



 

## <a name="remarks"></a>Hinweise

Die [IApplicationDocumentLists::GetList-Methode](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) kann verwendet werden, um die Windows Shell-MRU-Liste für die Menübandanwendung abzurufen. Das von dieser Methode abgerufene Objekt kann dann von der Anwendung verwendet werden,  um die Daten zu erstellen, die vom Menübandframework zum Auffüllen der Liste Zuletzt verwendeter Elemente des Anwendungsmenüs [benötigt werden.](windowsribbon-controls-applicationmenu.md)

> [!Note]  
> Bei Verwendung dieser Methode sollte *listtype* den Wert `ADLT_RECENT` haben.

 

Ein Beispiel zum Implementieren einer MRU-Elementliste in einer Menübandframeworkanwendung finden Sie im [HTMLEditRibbon-Beispiel.](windowsribbon-htmleditribbonsample.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Markupelement "Zuletzt verwendete Elemente"**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 