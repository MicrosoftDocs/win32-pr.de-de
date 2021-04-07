---
title: Hosten eines Windows-losen ActiveX-Steuer Elements mit MSAA
description: Erfahren Sie, wie Sie einen Steuerelement Container erstellen, der fensterlose Microsoft-ActiveX-Steuerelemente hosten kann, die Microsoft Active Accessibility implementieren.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, fensterloses ActiveX-Steuerelement
- Fensterloses ActiveX-Steuerelement, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727521"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Hosten eines Windows-losen ActiveX-Steuer Elements mit MSAA

Erfahren Sie, wie Sie einen Steuerelement Container erstellen, der fensterlose Microsoft-ActiveX-Steuerelemente hosten kann, die Microsoft Active Accessibility implementieren. Wenn Sie die hier beschriebenen Schritte ausführen, können Sie sicherstellen, dass alle auf Microsoft Active Accessibility basierten, fensterlosen Steuerelemente, die in Ihrem Steuerelement Container gehostet werden, für die Hilfstechnologie (at)-Client Anwendungen verfügbar sind.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmierung von Microsoft Win32 und Component Object Model (com)
-   Fensterlose ActiveX-Steuerelemente
-   Microsoft Active Accessibility-Server

## <a name="instructions"></a>Anweisungen

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Schritt 1: Stellen Sie die Schnittstelle "IAccessible" im Namen des fensterlosen Steuer Elements bereit.

Wenn das System den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Zeiger für den Stamm eines fensterlosen Steuer Elements benötigt, fragt das System den Steuerelement Container ab. Zum Abrufen des Zeigers ruft der Container die Implementierung der [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) -Methode des fensterlosen Steuer Elements auf.

Wenn der Steuerelement Container über eine Microsoft Active Accessibility-Implementierung verfügt, kann er den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Zeiger des fensterlosen Steuer Elements auf das System zurückgeben.

Wenn der Steuerelement Container eine Microsoft UI Automation-Implementierung aufweist, rufen Sie die [**uiaproviderfromiaccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) -Funktion auf, um einen [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstellen Zeiger zu erhalten, der das Steuerelement darstellt, und geben Sie dann den **IRawElementProviderSimple** -Schnittstellen Zeiger an das System zurück.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Schritt 2: Antworten auf die WM- \_ GetObject-Nachricht im Namen des fensterlosen Steuer Elements.

Wenn eine Client Anwendung auf ein WinEvent antwortet, das von einem fensterlosen Steuerelement ausgelöst wird, empfängt der Steuerelement Container eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht für das Steuerelement. Die Meldung enthält die Objekt-ID des fensterlosen Steuer Elements, das das Ereignis ausgelöst hat.

Der Steuerelement Container antwortet, indem er das fensterlose Steuerelement sucht, das die Objekt-ID besitzt, und dann die [**iaccessibleobjectfromid**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) -Methode dieses Steuer Elements aufruft. Die **AccessibleObjectFromID** -Methode gibt den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger für das UI-Element zurück, und der Steuerelement Container gibt den Zeiger auf das System zurück, das diese an die Client Anwendung weiterleitet.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Schritt 3: Implementieren Sie die iaccessiblewindowlesssite-Schnittstelle.

1.  Implementieren Sie die [**iaccessiblewindowlesssite:: getparameentaccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) -Methode.

    Wenn eine Client Anwendung Barrierefreiheits Informationen über das übergeordnete Element des Stamm Anbieters des fensterlosen Steuer Elements benötigt, ruft das System die [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) -Methode des fensterlosen Steuer Elements auf. Das-Steuerelement antwortet, indem er die [**iaccessiblewindowlesssite:: getParser**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) -Methode des Steuerelement Containers aufruft, die den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Zeiger auf das übergeordnete Element des fensterlosen Steuer Elements bereitstellt.

2.  Implementieren Sie die Methoden [**iaccessiblewindowlesssite:: acquireobjectidrange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**queryobjectidrange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)und [**releaseobjectidrange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) .

    Der Steuerelement Container muss eine Zuordnung von Objekt-ID-Bereichen zu fensterlosen Steuerelementen aufrechterhalten. Die Zuordnung ermöglicht es dem Steuerelement Container, das Steuerelement zu identifizieren, das auf eine bestimmte Anforderung für eine Objekt-ID reagieren soll. Die folgende Tabelle zeigt ein Beispiel für das Mapping von Objekt-ID-Bereichen zu fensterlosen Steuerelementen.

    

    | Bereichs Basis | Bereichs Größe | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Steuerelement 1 |
    | 1500       | 1000       | Steuerung 2 |
    | 2500       | 2000       | Steuerelement 1 |

    

     

    Der Steuerelement Container muss die Zuordnung von Objekt-ID-Bereichen zu fensterlosen Steuerelementen für sich selbst und alle fensterlosen untergeordneten Elemente aufrechterhalten. Die Objekt-ID-Bereiche müssen nicht nebeneinander angeordnet werden. Um Denial-of-Service-Angriffe zu vermeiden, kann der Steuerelement Container außerdem Grenzwerte für die Anzahl der Bereiche festlegen, die einem bestimmten Steuerelement erteilt werden. Es ist jedoch sinnvoll, mehr als einen Bereich pro Steuerelement zuzulassen, damit ein Steuerelement vergrößert werden kann.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Schritt 4: optional: Implementieren Sie die iaccessiblehostingelementproviders-Schnittstelle.

Implementieren Sie die [**iaccessiblehostingelementproviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) -Schnittstelle, wenn Ihr Steuerelement Container über eine Microsoft Active Accessibility Server-Implementierung verfügt und der Server der Stamm einer Barrierefreiheits Struktur ist, die fensterlose ActiveX-Steuerelemente enthält, die die Benutzeroberflächen Automatisierung unterstützen. Die **iaccessiblehostingelementproviders** -Schnittstelle verfügt über eine einzelne Methode, [**getembeddedfragmentroots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), mit der die [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) -Schnittstellen Zeiger von allen fensterlosen ActiveX-Steuerelementen der Benutzeroberflächen Automatisierung abgerufen werden, die von Ihrem Steuerelement Container gehostet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Barrierefreiheit für das fensterlose ActiveX-Steuerelement](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 