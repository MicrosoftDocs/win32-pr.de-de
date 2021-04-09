---
title: Eigenschaftenblätter und Eigenschaftenseiten
description: Eigenschaftenblätter und Eigenschaftenseiten
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cc61d1e1ed0cb833632b6b627a0c683a3cb0e4
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "103869319"
---
# <a name="property-sheets-and-property-pages"></a>Eigenschaftenblätter und Eigenschaftenseiten

Die Eigenschaften eines Objekts werden für Clients genauso wie Methoden über COM-Schnittstellen oder die **IDispatch** -Implementierung des Objekts verfügbar gemacht, sodass Eigenschaften durch Programme, die diese Methoden aufrufen, geändert werden können. Die OLE-Technologie von Eigenschaften Seiten bietet die Möglichkeit zum Erstellen einer Benutzeroberfläche für die Eigenschaften eines Objekts gemäß den Windows-Benutzeroberflächen Standards. Folglich werden die Eigenschaften den Endbenutzern zur Verfügung gestellt. Das Eigenschaften Blatt eines Objekts ist ein Dialogfeld, in dem jede Registerkarte einer bestimmten Eigenschaften Seite entspricht. Das OLE-Modell zum Arbeiten mit Eigenschaften Seiten besteht aus den folgenden Features:

-   Jede Eigenschaften Seite wird von einem Prozess internen Objekt verwaltet, das entweder [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) oder [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)implementiert. Jede Seite wird mit einer eigenen eindeutigen CLSID identifiziert.
-   Ein-Objekt gibt die Unterstützung für Eigenschaften Seiten durch Implementieren von [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)an. Über diese Schnittstelle kann der Aufrufer eine Liste von CLSIDs abrufen, die die spezifischen Eigenschaften Seiten identifizieren, die das Objekt unterstützt. Wenn das-Objekt eine CLSID einer Eigenschaften Seite angibt, muss das Objekt in der Lage sein, Eigenschafts Änderungen von der Eigenschaften Seite zu empfangen.
-   Jeder Code Abschnitt (Client oder Objekt), der das Eigenschaften Blatt eines Objekts anzeigen möchte, übergibt den [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Zeiger des Objekts (oder ein Array, wenn mehrere Objekte betroffen sind) zusammen mit einem Array von seitenclsids an [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) oder [**olecreatepropertyframeindirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), das das Dialogfeld im Registerkarten Format erstellt.
-   Im Dialogfeld "Eigenschaften Rahmen" wird eine einzelne Instanz jeder Eigenschaften Seite mithilfe von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) für jede CLSID instanziiert. Der Eigenschafts Rahmen erhält mindestens einen [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) -Zeiger für jede Seite. Außerdem erstellt der Frame ein Eigenschaften Seiten-Website Objekt in sich selbst für jede Seite. An jedem Standort wird [**ipropertypagesite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) implementiert, und dieser Zeiger wird an jede Seite übermittelt. Die Seite kommuniziert dann über diesen Schnittstellen Zeiger mit der Website.
-   Jede Seite wird auch von dem Objekt oder den Objekten, für die es aufgerufen wurde, informiert. Das heißt, der Eigenschafts Rahmen übergibt die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)-Zeiger der Objekte an jede Seite. Wenn Sie angewiesen werden, Änderungen auf die Objekte anzuwenden, fragt jede Seite den entsprechenden Schnittstellen Zeiger ab und übergibt neue Eigenschaftswerte an die Objekte in der gewünschten Weise. Es gibt keine Bestimmungen zur Art der Kommunikation.
-   Ein Objekt kann auch pro Eigenschaft durchsuchen durch die [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) -Schnittstelle unterstützen, sodass das-Objekt angeben kann, welche Eigenschaft den Anfangs Fokus erhalten soll, wenn die Eigenschaften Seite angezeigt wird, und Zeichen folgen und Werte angeben, die vom Client auf der eigenen Benutzeroberfläche angezeigt werden können.

Diese Features sind in der folgenden Abbildung dargestellt:

![Diagramm, in dem die Eigenschaften Blätter und Eigenschaften Seiten Features angezeigt werden.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

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

Die [**ISpecifyPropertyPages:: GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) -Methode gibt ein Gezähltes Array von UUID-Werten (GUID) zurück, von denen jede die CLSID einer Eigenschaften Seite beschreibt, die das Objekt anzeigen soll. Wer das Eigenschaften Blatt mit [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) oder [**olecreatepropertyframeindirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) aufruft, übergibt dieses Array an die Funktion. Beachten Sie Folgendes: Wenn der Aufrufer Eigenschaften Seiten für mehrere Objekte anzeigen möchte, darf er nur die Schnittmenge der CLSID-Listen aller-Objekte an diese Funktionen übergeben. Dies bedeutet, dass der Aufrufer nur Eigenschaften Seitenaufrufen muss, die allen Objekten gemeinsam sind.

Außerdem übergibt der Aufrufer auch die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Zeiger auf die betroffenen Objekte an die API-Funktionen. Beide API-Funktionen erstellen ein Dialogfeld für den Eigenschaften Rahmen und instanziieren eine Seiten Website mit [**ipropertypagesite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) für jede Seite, die geladen wird. Über diese Schnittstelle kann eine Eigenschaften Seite folgende Aktionen ausführen:

-   Rufen Sie die aktuelle Sprache ab, die im Eigenschaften Blatt durch [**getlocaleid**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid)verwendet wird.
-   Bitten Sie den Frame, Tastatureingaben über [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator)zu verarbeiten.
-   Hiermit Benachrichtigen Sie den Rahmen der Änderungen auf der Seite über [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Rufen Sie einen Schnittstellen Zeiger für den Frame selbst über [**getpagecontainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer)ab, obwohl zurzeit keine Schnittstellen für den Frame definiert sind. für diese Funktion wird immer E \_ notimpl zurückgegeben.

Der Eigenschafts Rahmen instanziiert jedes Eigenschaften Seiten Objekt und ruft die [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) -Schnittstelle jeder Seite ab. Über diese Schnittstelle informiert der Frame die Seite der Seiten Seite ([**setpagesite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), ruft Seiten Dimensionen und Zeichen folgen ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)) ab, übergibt die Schnittstellen Zeiger an die betroffenen Objekte ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)) und teilt der Seite mit, wann die Steuerelemente erstellt und zerstört werden sollen ([**aktivieren**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) und [**Deaktivieren**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)). weist die Seite an, sich selbst anzuzeigen oder neu zu positionieren ([**anzeigen**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) und [**verschieben**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), weist die Seite an, die aktuellen Werte auf die betroffenen Objekte anzuwenden ([**anwenden**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), überprüft den geänderten Status der Seite ([**ispagedirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), ruft Hilfe ([**Hilfe**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) auf und übergibt Tastatureingaben an die Seite ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Ein Objekt kann auch das Durchsuchen pro Eigenschaft unterstützen, das Folgendes bietet:

1.  Eine Methode (über [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) und [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)), um anzugeben, welche Eigenschaft, auf der die Eigenschaften Seite beim ersten Anzeigen eines Eigenschaften Blatts den Anfangs Fokus erhalten soll.
2.  Eine Methode (über [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) für das-Objekt, um vordefinierte Werte und entsprechende beschreibende Zeichen folgen anzugeben, die auf der Benutzeroberfläche eines Clients für Eigenschaften angezeigt werden können.

Ein-Objekt kann (2) ohne Unterstützung (1) unterstützen, z. b. wenn das-Objekt über kein Eigenschaften Blatt verfügt.

Die [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) -Schnittstelle und die [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) -Schnittstelle werden wie folgt definiert:

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

Um die Unterstützung für diese Funktionen anzugeben, implementiert das Objekt [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). Über diese Schnittstelle kann der Aufrufer die zum Durchsuchen erforderlichen Informationen anfordern, z. b. vordefinierte Zeichen folgen ([**getpredefinedstrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) und Werte ([**getpredefinedvalue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)) sowie eine Anzeige Zeichenfolge für eine bestimmte Eigenschaft ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Außerdem kann der Client die CLSID der Eigenschaften Seite abrufen, die es dem Benutzer ermöglicht, eine bestimmte Eigenschaft zu bearbeiten, die mit einer DISPID ([**mappropertytopage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)) identifiziert wird. Der Client weist dann den Eigenschaften Rahmen an, diese Seite zu aktivieren, indem er die CLSID und die DISPID an [**olecreatepropertyframeindirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)übergibt. Der Frame aktiviert diese Seite zuerst und übergibt die DISPID über [**IPropertyPage2:: editproperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty)an die Seite. Die Seite legt dann den Fokus auf das Bearbeitungsfeld dieser Eigenschaft fest. Auf diese Weise kann ein Client von einem Eigenschaftsnamen in seiner eigenen Benutzeroberfläche zu der Eigenschaften Seite springen, die diese Eigenschaft bearbeiten kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften Seiten und Eigenschaften Blätter](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




