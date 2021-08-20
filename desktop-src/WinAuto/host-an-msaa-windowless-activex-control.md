---
title: Hosten eines fensterlosen MSAA-steuerelements ActiveX
description: Erfahren Sie, wie Sie einen Steuerelementcontainer erstellen, der fensterlose Microsoft ActiveX-Steuerelemente hosten kann, die Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, Fensterloses ActiveX-Steuerelement
- Fensterloses ActiveX,MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d086fdc33c1b645294827ec62784612ffeb617f12caf5a101ea8472da3e765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115131"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Hosten eines fensterlosen MSAA-steuerelements ActiveX

Erfahren Sie, wie Sie einen Steuerelementcontainer erstellen, der fensterlose Microsoft ActiveX-Steuerelemente hosten kann, die Microsoft Active Accessibility. Mithilfe der hier beschriebenen Schritte können Sie sicherstellen, dass alle Microsoft Active Accessibility-basierten fensterlosen Steuerelemente, die in Ihrem Steuerelementcontainer gehostet werden, für Hilfstechnologieclientanwendungen (AT) zugänglich sind.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [ActiveX-Steuerelemente](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Microsoft Win32- und Component Object Model-Programmierung (COM)
-   Fensterlose ActiveX Steuerelemente
-   Microsoft Active Accessibility Server

## <a name="instructions"></a>Anweisungen

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Schritt 1: Geben Sie die IAccessible-Stammschnittstelle im Namen des fensterlosen Steuerelements an.

Wenn das System den [**IAccessible-Zeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für den Stamm eines fensterlosen Steuerelements benötigt, fragt das System den Steuerelementcontainer ab. Um den Zeiger abzurufen, ruft der Container die Implementierung der [**IServiceProvider::QueryService-Methode**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) des fensterlosen Steuerelements auf.

Wenn der Steuerelementcontainer über eine Microsoft Active Accessibility verfügt, kann er den [**IAccessible-Zeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des fensterlosen Steuerelements auf das System zurückgeben.

Wenn der Steuerelementcontainer über eine Microsoft Benutzeroberflächenautomatisierung-Implementierung verfügt, rufen Sie die [**UiaProviderFromIAccessible-Funktion**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) auf, um einen [**IRawElementProviderSimple-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) zu erhalten, der das Steuerelement darstellt, und geben Sie dann den **IRawElementProviderSimple-Schnittstellenzeiger** an das System zurück.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Schritt 2: Reagieren sie im Namen des fensterlosen Steuerelements auf die WM \_ GETOBJECT-Nachricht.

Wenn eine Clientanwendung auf ein WinEvent antwortet, das von einem fensterlosen Steuerelement ausgelöst wird, empfängt der Steuerelementcontainer im Namen des Steuerelements eine [**WM \_ GETOBJECT-Nachricht.**](wm-getobject.md) Die Nachricht enthält die Objekt-ID des fensterlosen Steuerelements, das das Ereignis ausgelöst hat.

Der Steuerelementcontainer reagiert, indem er nach dem fensterlosen Steuerelement sucht, das die Objekt-ID "besitzt" und dann die [**IAccessibleHandler::AccessibleObjectFromID-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) dieses Steuerelements aufruft. Die **AccessibleObjectFromID-Methode** gibt den [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das Benutzeroberflächenelement zurück, und der Steuerelementcontainer gibt den Zeiger auf das System zurück, das ihn an die Clientanwendung weiterleite.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Schritt 3: Implementieren Sie die IAccessibleWindowlessSite-Schnittstelle.

1.  Implementieren Sie [**die IAccessibleWindowlessSite::GetParentAccessible-Methode.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible)

    Wenn eine Clientanwendung Barrierefreiheitsinformationen über das übergeordnete Element des Stammanbieters des fensterlosen Steuerelements benötigt, ruft das System die [**IAccessible::get \_ accParent-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) des fensterlosen Steuerelements auf. Das Steuerelement antwortet, indem es die [**IAccessibleWindowlessSite::GetParentAccessible-Methode**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) des Steuerelementcontainers aufruft, die den [**IAccessible-Zeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des übergeordneten Steuerelements des fensterlosen Steuerelements zur Verfügung stellt.

2.  Implementieren Sie [**die Methoden IAccessibleWindowlessSite::AcquireObjectIdRange,**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)und [**ReleaseObjectIdRange.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange)

    Ihr Steuerelementcontainer muss eine Zuordnung von Objekt-ID-Bereichen zu fensterlosen Steuerelementen verwalten. Die Zuordnung ermöglicht es dem Steuerelementcontainer, das Steuerelement zu identifizieren, das auf eine bestimmte Anforderung für eine Objekt-ID reagieren soll. Die folgende Tabelle zeigt ein Beispiel für die Zuordnung von Objekt-ID-Bereichen zu fensterlosen Steuerelementen.

    

    | Bereichsbasis | Bereichsgröße | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Steuerung 1 |
    | 1500       | 1000       | Steuerung 2 |
    | 2500       | 2000       | Steuerung 1 |

    

     

    Der Steuerelementcontainer muss die Zuordnung von Objekt-ID-Bereichen zu fensterlosen Steuerelementen für sich selbst und alle fensterlosen children-Objekte verwalten. Die Objekt-ID-Bereiche müssen nicht nebeneinander liegen. Um Denial-of-Service-Angriffe zu vermeiden, kann der Steuerungscontainer außerdem Grenzwerte für die Anzahl der Bereiche setzen, die einer bestimmten Steuerung gewährt werden. Es ist jedoch hilfreich, mehr als einen Bereich pro Steuerelement zu erlauben, damit ein Steuerelement wachsen kann.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Schritt 4: Optional: Implementieren Sie die IAccessibleHostingElementProviders-Schnittstelle.

Implementieren Sie die [**IAccessibleHostingElementProviders-Schnittstelle,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) wenn Ihr Steuerelementcontainer über eine Microsoft Active Accessibility-Serverimplementierung verfügt und der Server der Stamm einer Barrierefreiheitsstruktur ist, die fensterlose ActiveX-Steuerelemente enthält, die Benutzeroberflächenautomatisierung. Die **IAccessibleHostingElementProviders-Schnittstelle** verfügt über eine einzelne Methode, [**GetEmbeddedFragmentRoots,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots)die die [**IRawElementProviderFragmentRoot-Schnittstellenzeige**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) aller Benutzeroberflächenautomatisierung ActiveX-Steuerelemente abruft, die von Ihrem Steuerelementcontainer gehostet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hosten eines fensterlosen Benutzeroberflächenautomatisierung-Steuerelements ActiveX Steuerelements](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Fensterloses ActiveX Barrierefreiheit](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 