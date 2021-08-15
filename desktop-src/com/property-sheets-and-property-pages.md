---
title: Eigenschaftenblätter und Eigenschaftenseiten
description: Eigenschaftenblätter und Eigenschaftenseiten
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991ea650838e9980292257c14d26909e9476f0f35422fa21deab2b0b5ecbbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104933"
---
# <a name="property-sheets-and-property-pages"></a>Eigenschaftenblätter und Eigenschaftenseiten

Die Eigenschaften eines Objekts werden für Clients genauso wie Methoden über COM-Schnittstellen oder die **IDispatch-Implementierung** des Objekts verfügbar gemacht, sodass Eigenschaften durch Programme geändert werden können, die diese Methoden aufrufen. Die OLE-Technologie von Eigenschaftenseiten bietet die Möglichkeit, eine Benutzeroberfläche für die Eigenschaften eines Objekts gemäß Windows Benutzeroberflächenstandards zu erstellen. Daher werden die Eigenschaften für Endbenutzer verfügbar gemacht. Das Eigenschaftenblatt eines Objekts ist ein Tabstoppdialogfeld, in dem jede Registerkarte einer bestimmten Eigenschaftenseite entspricht. Das OLE-Modell für die Arbeit mit Eigenschaftenseiten besteht aus den folgenden Features:

-   Jede Eigenschaftenseite wird von einem Prozessobjekt verwaltet, das entweder [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) oder [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)implementiert. Jede Seite wird mit ihrer eigenen eindeutigen CLSID identifiziert.
-   Ein -Objekt gibt seine Unterstützung für Eigenschaftenseiten an, indem [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)implementiert wird. Über diese Schnittstelle kann der Aufrufer eine Liste von CLSIDs abrufen, die die spezifischen Eigenschaftenseiten identifizieren, die das Objekt unterstützt. Wenn das -Objekt eine Eigenschaftenseiten-CLSID angibt, muss das Objekt In der Lage sein, Eigenschaftenänderungen von der Eigenschaftenseite zu empfangen.
-   Jeder Codeabschnitt (Client oder Objekt), der das Eigenschaftenblatt eines Objekts anzeigen möchte, übergibt den [**IUnknown-Zeiger**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) des Objekts (oder ein Array, wenn mehrere Objekte betroffen sein sollen) zusammen mit einem Array von Seiten-CLSIDs an [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) oder [**OleCreatePropertyFrameIndirect,**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)wodurch das Tabbed-Dialogfeld erstellt wird.
-   Der Eigenschaftenrahmendialog instanziiert eine einzelne Instanz jeder Eigenschaftenseite mit [**coCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) für jede CLSID. Der Eigenschaftenrahmen ruft mindestens einen [**IPropertyPage-Zeiger**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) für jede Seite ab. Darüber hinaus erstellt der Frame für jede Seite selbst ein Eigenschaftenseiten-Websiteobjekt. Jeder Standort implementiert [**IPropertyPageSite,**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) und dieser Zeiger wird an jede Seite übergeben. Die Seite kommuniziert dann über diesen Schnittstellenzeiger mit der Website.
-   Jede Seite wird auch auf das Objekt oder die Objekte aufmerksam gemacht, für die sie aufgerufen wurde. Das heißt, der Eigenschaftenrahmen übergibt die [**IUnknown-Zeiger**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)der Objekte an jede Seite. Wenn sie angewiesen wird, Änderungen auf die Objekte anzuwenden, fragt jede Seite den entsprechenden Schnittstellenzeiger ab und übergibt neue Eigenschaftswerte auf die gewünschte Weise an die Objekte. Es gibt keine Angaben dazu, wie eine solche Kommunikation erfolgen muss.
-   Ein Objekt kann auch das Durchsuchen der [**IPerPropertyBrowsing-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) pro Eigenschaft unterstützen, sodass das Objekt angeben kann, welche Eigenschaft den anfangs Fokus erhalten soll, wenn die Eigenschaftenseite angezeigt wird, und Zeichenfolgen und Werte anzugeben, die vom Client auf seiner eigenen Benutzeroberfläche angezeigt werden können.

Diese Features sind im folgenden Diagramm dargestellt:

![Diagramm, das die Eigenschaftenblätter und Eigenschaftenseitenfeatures zeigt.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

Diese Schnittstellen werden wie folgt definiert:

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

Die [**ISpecifyPropertyPages::GetPages-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) gibt ein gezähltes Array von UUID-Werten (GUID) zurück, die jeweils die CLSID einer Eigenschaftenseite beschreiben, die das Objekt anzeigen möchte. Jeder, der das Eigenschaftenblatt mit [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) oder [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) aufruft, übergibt dieses Array an die Funktion. Beachten Sie Folgendes: Wenn der Aufrufer Eigenschaftenseiten für mehrere Objekte anzeigen möchte, darf er nur die Schnittmenge der CLSID-Listen aller Objekte an diese Funktionen übergeben. Anders ausgedrückt: Der Aufrufer darf nur Eigenschaftenseiten aufrufen, die allen Objekten gemeinsam sind.

Darüber hinaus übergibt der Aufrufer die [**IUnknown-Zeiger**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) an die betroffenen Objekte auch an die API-Funktionen. Beide API-Funktionen erstellen ein Eigenschaftenrahmendialogfeld und instanziieren eine Seitenwebsite mit [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) für jede Seite, die geladen wird. Über diese Schnittstelle kann eine Eigenschaftenseite:

-   Rufen Sie die aktuelle Sprache ab, die im Eigenschaftenblatt über [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid)verwendet wird.
-   Bitten Sie den Frame, Tastatureingaben über [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator)zu verarbeiten.
-   Benachrichtigen Sie den Frame über Änderungen auf der Seite über [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Rufen Sie über [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer)einen Schnittstellenzeiger für den Frame selbst ab, obwohl derzeit keine Schnittstellen für den Frame definiert sind, gibt diese Funktion immer E \_ NOTIMPL zurück.

Der Eigenschaftenrahmen instanziiert jedes Eigenschaftenseitenobjekt und ruft die [**IPropertyPage-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) jeder Seite ab. Über diese Schnittstelle informiert der Frame die Seite über seine Seitenwebsite ([**SetPageSite),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)ruft Seitendimensionen und Zeichenfolgen ab ([**GetPageInfo),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)übergibt die Schnittstellenzeiger an die betroffenen Objekte ([**SetObjects),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)teilt der Seite mit, wann die Steuerelemente erstellt und zerstört werden sollen ([**Aktivieren**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) und [**Deaktivieren),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)weist die Seite an, anzuzeigen. oder sich selbst neu positionieren ([**Anzeigen**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) und [**Verschieben),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)weist die Seite an, ihre aktuellen Werte auf die betroffenen Objekte anzuwenden ([**Anwenden),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)überprüft den geänderten Status der Seite ([**IsPageDirty),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)ruft hilfe ([**Hilfe**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) auf und übergibt Tastatureingaben an die Seite ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Ein Objekt kann auch das Durchsuchen pro Eigenschaft unterstützen, was:

1.  Eine Möglichkeit (über [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) und [**IPropertyPage2),**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)um anzugeben, welche Eigenschaft auf welcher Eigenschaftenseite den anfänglichen Fokus erhalten soll, wenn ein Eigenschaftenblatt zum ersten Mal angezeigt wird
2.  Eine Möglichkeit (über [**IPerPropertyBrowsing)**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)für das -Objekt, vordefinierte Werte und entsprechende beschreibende Zeichenfolgen anzugeben, die in einer clienteigenen Benutzeroberfläche für Eigenschaften angezeigt werden können.

Ein Objekt kann (2) ohne Unterstützung (1) unterstützen, z. B. wenn das Objekt über kein Eigenschaftenblatt verfügt.

Die Schnittstellen [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) und [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) sind wie folgt definiert:

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

Um die Unterstützung für solche Funktionen anzugeben, implementiert das -Objekt [**IPerPropertyBrowsing.**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) Über diese Schnittstelle kann der Aufrufer die zum Durchsuchen erforderlichen Informationen anfordern, z. B. vordefinierte Zeichenfolgen ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) und Werte ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)) sowie eine Anzeigezeichenfolge für eine bestimmte Eigenschaft ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Darüber hinaus kann der Client die CLSID der Eigenschaftenseite abrufen, die es dem Benutzer ermöglicht, eine bestimmte Eigenschaft zu bearbeiten, die mit einer DISPID identifiziert wird ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). Der Client weist dann den Eigenschaftenrahmen an, diese Seite zunächst zu aktivieren, indem er die CLSID und die DISPID an [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)übergibt. Der Frame aktiviert diese Seite zuerst und übergibt die DISPID über [**IPropertyPage2::EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty)an die Seite. Die Seite legt dann den Fokus auf das Bearbeitungsfeld dieser Eigenschaft fest. Auf diese Weise kann ein Client von einem Eigenschaftennamen in seiner eigenen Benutzeroberfläche zur Eigenschaftenseite springen, die diese Eigenschaft bearbeiten kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftenseiten und Eigenschaftenblätter](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




