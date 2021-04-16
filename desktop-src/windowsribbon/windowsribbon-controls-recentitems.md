---
title: Zuletzt verwendete Elemente
description: Die Liste der zuletzt verwendeten Elemente ist ein Bereich im Anwendungsmenü, in dem die zuletzt verwendeten Elemente (MRU) für eine Anwendung angezeigt werden.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104571556"
---
# <a name="recent-items"></a>Zuletzt verwendete Elemente

Die Liste der zuletzt verwendeten Elemente ist ein Bereich im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) , in dem die zuletzt verwendeten Elemente (MRU) für eine Anwendung angezeigt werden.

-   [Details](#details)
-   [Eigenschaften für zuletzt verwendete Elemente](#recent-items-properties)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht eine Liste zuletzt verwendeter Elemente aus WordPad für Windows 7.

![Screenshot der Liste der zuletzt verwendeten Elemente im Microsoft Paint-Menüband.](images/controls/recentitems.png)

Das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) kann höchstens eine [**applicationmenu. recentitems**](windowsribbon-element-applicationmenu-recentitems.md) -Liste enthalten, die durch ein **applicationmenu. recentitems** -Element dargestellt wird, um aktuelle Dokumente, Bilder, Filme und andere Projekte anzuzeigen, an denen ein Benutzer gearbeitet hat. Die Anzahl der aufgelisteten Elemente liegt zwischen 0 (null) und der maximalen Anzahl, die im Markup angegeben ist. der Standardwert ist 10. Die zuletzt verwendeten Elemente werden als eine nummerierte Liste von Zeichen folgen angezeigt, die Dateinamen angeben. Es wird empfohlen, die [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md) -Eigenschaft zu verwenden, um den vollständigen Pfad für den Datei Speicherort anzugeben, wie im folgenden Screenshot gezeigt.

![Screenshot einer Liste zuletzt verwendeter Elemente in einem Anwendungsmenü.](images/overviews/applicationmenu-menurecentitems.png)

Das [**recentitems**](windowsribbon-element-recentitems.md) -Element verfügt über ein *enablepinning* -Attribut, das, wenn es auf festgelegt `true` ist, auf der rechten Seite jedes Elements in der Liste ein Pin-Symbol anzeigt, wie im folgenden Screenshot gezeigt.

> [!Note]  
> Das anhepup ist standardmäßig aktiviert, wenn das Attribut " *enablepinning* " nicht angegeben wird.

 

![Screenshot der letzten Elemente, die in einem Anwendungsmenü fixiert werden.](images/overviews/applicationmenu-menurecentitemspinned.png)

Der Fixierungs Algorithmus soll verhindern, dass Elemente aus der Liste der **zuletzt verwendeten Elemente** entfernt werden. Der Algorithmus erzeugt das folgende Verhalten:

-   Ein neues Element wird immer am oberen Rand der Liste **zuletzt geöffnete Elemente** hinzugefügt.
-   Elemente werden im Laufe der Zeit in der Liste nach unten verschoben. Sobald die Liste voll ist (erreicht die maximale Anzahl der im Markup angegebenen Elemente), werden ältere Elemente am Ende der Liste entfernt, wenn neue Elemente am Anfang der Liste hinzugefügt werden.
-   Wenn ein Element bereits irgendwo in der Liste angezeigt wird, aber wieder darauf zugegriffen wird, wird es wieder an den Anfang der Liste verschoben.
-   Wenn ein Element fixiert ist, wird es immer noch in der Liste nach unten angezeigt, aber es wird nicht vom unteren Rand entfernt. Wenn die Liste voll ist, wird stattdessen das erste nicht angeheftete Element oberhalb des fixierten Elements entfernt, wenn der Liste ein neues Element hinzugefügt wird.
-   Wenn die Anzahl der fixierten Elemente jemals die maximal zulässige Anzahl von Elementen erreicht, werden der Liste keine neuen Elemente hinzugefügt, bis ein Element gelöst wird.

## <a name="recent-items-properties"></a>Eigenschaften für zuletzt verwendete Elemente

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Steuerelement "zuletzt verwendete Elemente".

In der Regel wird die Eigenschaft "zuletzt verwendete Elemente" in der Multifunktionsleisten-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der Methode [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Steuerelement zuletzt verwendete Elemente zugeordnet sind.



| Eigenschafts Schlüssel                                                                       | Notizen                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)           | Kann nur durch Invalidierung aktualisiert werden. |
| [Benutzeroberflächen- \_ pkey- \_ entitems](windowsribbon-reference-properties-uipkey-recentitems.md) | Kann nur durch Invalidierung aktualisiert werden. |



 

## <a name="remarks"></a>Bemerkungen

Die [iapplicationdocumentlists:: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) -Methode kann verwendet werden, um die MRU-Liste der Windows-Shell für die Menüband-Anwendung abzurufen. Das von dieser Methode abgerufene-Objekt kann dann von der Anwendung verwendet werden, um die Daten zu erstellen, die für das Menüband-Framework zum Auffüllen der Liste zuletzt verwendeter **Elemente** im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)benötigt werden.

> [!Note]  
> Wenn Sie diese Methode verwenden, sollte *Listentyp* den Wert aufweisen `ADLT_RECENT` .

 

Ein Beispiel für das Implementieren einer MRU-Elementliste in einer Menüband-Framework-Anwendung finden Sie im [Beispiel htmleditribbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Zuletzt verwendete Elemente (Markup Element)**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 