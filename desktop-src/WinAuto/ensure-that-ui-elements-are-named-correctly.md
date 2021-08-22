---
title: Sicherstellen, dass Benutzeroberflächenelemente ordnungsgemäß benannt sind
description: In diesem Thema wird die richtige Methode zum Angeben der Namen der Benutzeroberflächenelemente in Ihren Microsoft Win32-Anwendungen beschrieben, sodass Microsoft Active Accessibility die Namen für Clientanwendungen über IAccessible \ 32 genau verfügbar machen kann. Name-Eigenschaft.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c047228159e011ffa9a0842f1748ee07e6af4a49ff296ae8ed65b494b8c53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052788"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>Sicherstellen, dass Benutzeroberflächenelemente ordnungsgemäß benannt sind

In diesem Thema wird die richtige Methode zum Angeben der Namen der Benutzeroberflächenelemente in Ihren Microsoft Win32-Anwendungen beschrieben, sodass Microsoft Active Accessibility die Namen über die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name-Eigenschaft für Clientanwendungen genau verfügbar machen [kann.](name-property.md)

Die Informationen in diesem Abschnitt gelten nur für Microsoft Active Accessibility Daten. Sie gilt nicht für Anwendungen, die Microsoft Benutzeroberflächenautomatisierung verwenden, oder solche, die auf Markupsprachen wie HTML, dynamischem HTML (DHTML) oder XML basieren.

-   [Übersicht](#overview)
-   [Wie falsche Benennung Probleme verursacht](#how-incorrect-naming-causes-problems)
-   [So ruft MSAA die Name-Eigenschaft ab](#how-msaa-gets-the-name-property)
-   [Suchen und Beheben von Benennungsproblemen](#how-to-find-and-correct-naming-problems)
-   [Richtiger Name einer Trackleiste](#how-to-correctly-name-a-trackbar)
-   [Verwenden unsichtbarer Bezeichnungen zum Benennen von Steuerelementen](#how-to-use-invisible-labels-to-name-controls)
-   [Verwenden der direkten Anmerkung zum Angeben der Name-Eigenschaft](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Schritte zum Kommentieren der Name-Eigenschaft](#steps-for-annotating-the-name-property)
    -   [Beispiel für das Kommentieren der Name-Eigenschaft](#example-of-annotating-the-name-property)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

In Microsoft Active Accessibility wird jedes Benutzeroberflächenelement in einer Anwendung durch ein -Objekt dargestellt, das die [**IAccessible-Schnittstelle verfügbar**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) macht. Clientanwendungen verwenden die Eigenschaften und Methoden der **IAccessible-Schnittstelle,** um mit dem Benutzeroberflächenelement zu interagieren und Informationen darüber abzurufen. Eine der wichtigsten Eigenschaften, die von der **IAccessible-Schnittstelle verfügbar** gemacht werden, ist die [Name-Eigenschaft](name-property.md). Clientanwendungen verwenden die Eigenschaft Name, um ein Benutzeroberflächenelement für den Benutzer zu suchen, zu identifizieren oder ankündigen zu können. Wenn Microsoft Active Accessibility die Name-Eigenschaft eines bestimmten Benutzeroberflächenelements nicht ordnungsgemäß verfügbar machen kann, können Clientanwendungen das Benutzeroberflächenelement dem Benutzer nicht präsentieren, und Benutzer mit Behinderungen können nicht auf das Benutzeroberflächenelement zugreifen.

## <a name="how-incorrect-naming-causes-problems"></a>Wie falsche Benennung Probleme verursacht

Um die Probleme zu veranschaulichen, die durch eine falsche Benennung von Benutzeroberflächenelementen verursacht werden, sollten Sie das in der folgenden Abbildung dargestellte Formular für die Namenseingabe berücksichtigen.

![Abbildung eines einfachen Formulars für die Eingabe von Vor- und Nachname](images/incorrect-form.png)

Obwohl die Benutzeroberflächenelemente im Formular in Ordnung aussehen, ist die programmgesteuerte Implementierung falsch. Für einen Microsoft Active Accessibility-Client, z. B. eine Sprachausgabe, ist die [Name-Eigenschaft](name-property.md) des oberen Bearbeitungssteuerpunkts "Nachname:", und die Name-Eigenschaft des unteren Bearbeitungssteuerpunkts ist eine leere Zeichenfolge (""). Die Sprachausgabe liest das oberste Bearbeitungssteuer steuerelement als "Nachname", obwohl der Benutzer den Vornamen eingeben muss. Die Sprachausgabe liest das zweite Bearbeitungssteuer steuerelement als "Kein Name", sodass der Benutzer keine Vorstellung davon hat, was in das zweite Bearbeitungssteuer steuerelement eingelesen werden soll. Die Sprachausgabe kann den Benutzer nicht bei der Eingabe von Daten in dieses einfache Formular unterstützen.

Ein weiteres Problem mit dem Formular ist, dass keinem der Bearbeitungssteuerelemente Tastenkombinationen zugewiesen sind. Der Benutzer wird gezwungen, entweder mit der Tabulatorkarte zu den Steuerelementen zu klicken oder die Maus zu verwenden.

In den folgenden Abschnitten wird die Ursache dieser Probleme erläutert, und es werden Richtlinien für deren Korrektur beschrieben.

## <a name="how-msaa-gets-the-name-property"></a>So ruft MSAA die Name-Eigenschaft ab

Microsoft Active Accessibility ruft die [Name-Eigenschaftenzeichenfolge](name-property.md) abhängig vom Typ des Benutzeroberflächenelements von verschiedenen Speicherorten ab. Für die meisten Benutzeroberflächenelemente, denen Fenstertext zugeordnet ist, Microsoft Active Accessibility fenstertext als Name-Eigenschaftenzeichenfolge verwendet. Beispiele für diese Art von Benutzeroberflächenelement sind Steuerelemente wie Schaltflächen, Menüelemente und QuickInfos.

Bei den folgenden Steuerelementen ignoriert Microsoft Active Accessibility den Fenstertext und sucht stattdessen nach einer statischen Textbezeichnung (oder Gruppenfeldbezeichnung), die dem Steuerelement unmittelbar in der Registerkartenfolge voraus geht.

-   Kombinationsfelder
-   Datums- und Uhrzeitauswahl
-   Bearbeitungs- und Rich Edit-Steuerelemente
-   IP-Adresssteuerelemente
-   Listenfelder
-   Listenansichten
-   Statusleisten
-   Bildlaufleisten
-   Statische Steuerelemente mit dem \_ SS-SYMBOL- oder \_ SS-BITMAP-Stil
-   Trackbars
-   Strukturansichten

Wenn die oben genannten Steuerelemente nicht von statischen Textbezeichnungen begleitet werden oder die Bezeichnungen nicht ordnungsgemäß implementiert sind, kann Microsoft Active Accessibility Clientanwendungen nicht die richtige [Name-Eigenschaft](name-property.md) bereitstellen.

Die meisten der oben genannten Steuerelemente verfügen tatsächlich über zugeordneten Fenstertext. Der Ressourcen-Editor generiert automatisch den Fenstertext, der aus einer generischen Zeichenfolge wie "edit1" oder "listbox3" besteht. Entwickler können den generierten Fenstertext zwar durch aussagekräftigeren Text ersetzen, die meisten tun dies jedoch nie. Da der generierte Fenstertext für den Benutzer keine Bedeutung hat, Microsoft Active Accessibility ignoriert und stattdessen die zugehörige statische Textbezeichnung verwendet.

## <a name="how-to-find-and-correct-naming-problems"></a>Suchen und Beheben von Benennungsproblemen

Im Unter Wie falsche Benennung verursacht Probleme angezeigten Formular für die Namenseingabe ist die Ursache der Probleme, dass die Registerkarten reihenfolge der Steuerelemente falsch ist. Wenn Sie die Benutzeroberfläche mit einem Testtool wie [Inspect](inspect-objects.md) untersuchen, werden die Probleme mit der Objekthierarchie angezeigt. Der folgende Screenshot zeigt die fehlerhafte Objekthierarchie des Namenseingabeformulars, wie sie in Überprüfen angezeigt wird.

![Screenshot des Überprüfungstools mit einer falschen Objekthierarchie des Namenseingabeformulars](images/incorrect-object-hierarchy.png)

Beachten Sie im vorherigen Screenshot, dass die Objekthierarchie nicht mit der Struktur der Steuerelemente in der Benutzeroberfläche des Namenseingabeformulars übereinstimmen. Beachten Sie auch, dass [Inspect](inspect-objects.md) dem vorletzten Element den falschen Namen zugewiesen hat (es ist das Bearbeitungssteuerelement für die Eingabe des Vornamens und sollte ein namens "Vorname:" sein. Beachten Sie schließlich, dass Inspect keinen Namen für das letzte Element finden konnte (es ist das Bearbeitungssteuerelement für die Eingabe des Nachnamens und sollte den Namen "Nachname:" haben.

Das folgende Beispiel zeigt den Inhalt der Ressourcendatei für das Namenseingabeformular. Beachten Sie, dass die Reihenfolge der Registerkarten nicht mit der logischen Struktur der Steuerelemente konsistent ist, da sie auf der Benutzeroberfläche angezeigt werden. Beachten Sie auch, dass für die beiden Bearbeitungssteuerelemente keine Tastenkombinationen angegeben sind.

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

Um die Probleme mit dem Namenseingabeformular zu beheben, sollte die Ressourcendatei (RC) bearbeitet werden, um Tastenkombinationen anzugeben, und die Steuerelemente sollten in der folgenden Reihenfolge platziert werden:

1.  Die statische Textbezeichnung "&First Name:".
2.  Das Bearbeitungssteuer steuerelement für die Eingabe des Vornamens (IDC \_ EDIT1).
3.  Die statische &"Nachname:".
4.  Das Bearbeitungssteuer steuerelement für die Eingabe des Nachnamens (IDC \_ EDIT2).
5.  Die Standardschaltfläche "OK".

Das folgende Beispiel zeigt die korrigierte Ressourcendatei für das Namenseingabeformular:

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

Um Korrekturen an einer Ressourcendatei vorzunehmen, können Sie die Datei entweder direkt bearbeiten, oder Sie können das Tool für die Registerkarten reihenfolge in Microsoft Visual Studio. Sie können auf das Tool tabellarische Reihenfolge in Visual Studio, indem Sie  entweder STRG+D drücken oder im **Menü Format** die Tabulator reihenfolge auswählen.

Nach dem Korrigieren und Neuerstellen der Anwendung sieht die Benutzeroberfläche des Namenseingabeformulars wie zuvor aus. Allerdings stellt Microsoft Active Accessibility clientanwendungen nun die richtigen Namenseigenschaften zur Verfügung und setzt den Fokus ordnungsgemäß fest, wenn der Benutzer die Tastenkombinationen ALT+F oder ALT+L drückt. Außerdem zeigt [Inspect](inspect-objects.md) die richtige Objekthierarchie an, wie der folgende Screenshot zeigt.

![Screenshot des barrierefreien Explorer-Tools mit einer korrekten Objekthierarchie des Namenseingabeformulars](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>Richtiger Name einer Trackleiste

Stellen Sie beim Definieren einer Trackleiste (oder eines Schiebereglers) sicher, dass die statische Haupttextbezeichnung für die Trackleiste vor der Trackleiste angezeigt wird und dass die statischen Textbezeichnungen für die minimalen und maximalen Bereiche nach der Trackleiste angezeigt werden. Beachten Sie, Microsoft Active Accessibility die statische Textbezeichnung verwendet, die unmittelbar vor einem -Steuerelement als [Name-Eigenschaft für](name-property.md) das Steuerelement steht. Wenn Sie die statische Haupttextbezeichnung direkt vor der Trackleiste und die anderen Bezeichnungen danach platzieren, wird sichergestellt, dass Microsoft Active Accessibility die richtige Name-Eigenschaft für einen Client bietet.

Die folgende Abbildung zeigt eine typische Trackleiste mit einer statischen Haupttextbezeichnung namens "Speed" und statischen Textbezeichnungen für die minimalen ("min") und maximalen ("max") Bereiche.

![Abbildung eines Trackbar-Steuerelements, das über eine Hauptbezeichnung und Bezeichnungen für die minimalen und maximalen Bereiche verfügt](images/speed-trackbar.png)

Das folgende Beispiel zeigt die richtige Methode zum Definieren einer Trackleiste und ihrer statischen Textbezeichnungen in der Ressourcendatei:

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Verwenden unsichtbarer Bezeichnungen zum Benennen von Steuerelementen

Es ist nicht immer möglich oder wünschenswert, für jedes Steuerelement eine sichtbare Bezeichnung zu haben. Beispielsweise kann das Hinzufügen von Bezeichnungen zu unerwünschten Änderungen in der Darstellung der Benutzeroberfläche führen. In diesem Fall können Sie unsichtbare Bezeichnungen verwenden. Microsoft Active Accessibility verwendet weiterhin den Text, der einer unsichtbaren Bezeichnung zugeordnet ist, aber die Bezeichnung wird nicht in der visuellen Benutzeroberfläche angezeigt oder beeinträchtigt.

Wie bei sichtbaren Bezeichnungen muss eine unsichtbare Bezeichnung dem Steuerelement in der Registerkartenfolge unmittelbar vorangeordnet sein. Um eine Bezeichnung in einer Ressourcendatei (RC) unsichtbar zu machen, fügen Sie oder dem Stilteil des statischen `NOT WS_VISIBLE` `|~WS_VISIBLE` Textsteuerfelds hinzu. Wenn Sie den Ressourcen-Editor in Visual Studio, können Sie die Visible-Eigenschaft auf False festlegen.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Verwenden der direkten Anmerkung zum Angeben der Name-Eigenschaft

Die Standardproxies, die in der Microsoft Active Accessibility-Laufzeitkomponente Oleacc.dll enthalten sind, stellen automatisch ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für alle Standardsteuerelemente Windows zur Verfügung. Wenn Sie ein standardes Windows-Steuerelement anpassen, geben die Standardproxies ihr Bestes, um alle **IAccessible-Eigenschaften** für Ihr benutzerdefiniertes Steuerelement genau zur Verfügung zu stellen. Sie sollten ein benutzerdefiniertes Steuerelement gründlich testen, um sicherzustellen, dass die Standardproxies genaue und vollständige Eigenschaftswerte bereitstellen. Wenn beim Testen ungenaue oder unvollständige Eigenschaftswerte angezeigt werden, können Sie möglicherweise die dynamische Anmerkungstechnik verwenden, die als direkte Anmerkung bezeichnet wird, um richtige Eigenschaftswerte zu liefern und fehlende Eigenschaftswerte hinzuzufügen.

Beachten Sie, dass die dynamische Anmerkung nicht nur für Steuerelemente gilt, die von Microsoft Active Accessibility Proxys unterstützt werden. Sie können sie auch verwenden, um Eigenschaften für jedes Steuerelement zu ändern oder zur Verfügung zu stellen, das eine eigene [**IAccessible-Implementierung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) bietet.

In diesem Abschnitt liegt der Schwerpunkt auf der Verwendung der direkten Anmerkung, um einen richtigen Wert für die [Name-Eigenschaft](name-property.md) des [**IAccessible-Objekts**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ein Steuerelement zu erhalten. Sie können auch direkte Anmerkungen verwenden, um andere Eigenschaftswerte zur Verfügung zu stellen. Darüber hinaus sind neben direkten Anmerkungen auch andere Techniken für dynamische Anmerkungen verfügbar, und die Features und Funktionen der API für dynamische Anmerkungen gehen weit über die in diesem Abschnitt beschriebenen Funktionen hinaus. Weitere Informationen zu dynamischen Anmerkungen finden Sie unter [Dynamic Annotation API](dynamic-annotation-api.md).

### <a name="steps-for-annotating-the-name-property"></a>Schritte zum Kommentieren der Name-Eigenschaft

Die Verwendung der direkten Anmerkung zum Ändern [der Name-Eigenschaft](name-property.md) eines Steuerelements umfasst die folgenden Schritte.

1.  Schließen Sie die folgenden Headerdateien ein:
    -   Initguid.h
    -   Oleacc.h

    > [!Note]  
    > Zum Definieren von GUIDs müssen Sie Initguid.h vor Oleacc.h in derselben Datei enthalten.

     

2.  Initialisieren Sie Component Object Model -Bibliothek (COM) durch Aufrufen der [CoInitializeEx-Funktion,](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in der Regel während des Anwendungsinitialisierungsprozesses.
3.  Erstellen Sie kurz nach der Erstellung des Zielsteuerelements (in der Regel während der [WM \_ INITDIALOG-Meldung)](../dlgbox/wm-initdialog.md) eine Instanz des Anmerkungs-Managers, und erhalten Sie einen Zeiger auf den [**IAccPropServices-Zeiger.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
4.  Kommentieren Sie die [Name-Eigenschaft des](name-property.md) Zielsteuer steuerelements mithilfe der [**IAccPropServices::SetHwndPropStr-Methode.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)

5.  Geben Sie [**den IAccPropServices-Zeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) frei.
6.  Bevor das Zielsteuerelement zerstört wird (in der Regel beim Behandeln der [WM \_ DESTROY-Nachricht),](../winmsg/wm-destroy.md) erstellen Sie eine Instanz des Anmerkungs-Managers und erhalten einen Zeiger auf seine [**IAccPropServices-Schnittstelle.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
7.  Verwenden Sie [**die IAccPropServices::ClearHwndProps-Methode,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) um die Name-Eigenschaftsanmerkungen aus dem Zielsteuerelement zu löschen. [](name-property.md)
8.  Geben Sie [**den IAccPropServices-Zeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) frei.
9.  Bevor Ihre Anwendung beendet wird (in der Regel während der Verarbeitung der [WM \_ DESTROY-Nachricht),](../winmsg/wm-destroy.md) geben Sie die COM-Bibliothek frei, indem Sie die [CoUninitialize-Funktion](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) aufrufen.

Die [**IAccPropServices::SetHwndPropStr-Funktion**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) nimmt fünf Parameter an. Die ersten drei -*hwnd*, *idObject* und *idChild -* werden kombiniert, um das Steuerelement zu identifizieren. Der vierte Parameter, *idProp,* gibt den Bezeichner der zu ändernden Eigenschaft an. Um die [Name-Eigenschaft zu ändern,](name-property.md)legen *Sie idProp* auf **PROPID ACC NAME \_ \_ fest.** (Eine Liste mit anderen Eigenschaften, die Sie über direkte Anmerkungen festlegen können, finden Sie unter [Using Direct Annotation](using-direct-annotation.md).) Der letzte Parameter von **SetHwndPropStr**, *str,* ist die neue Zeichenfolge, die als Name-Eigenschaft verwendet werden soll.

### <a name="example-of-annotating-the-name-property"></a>Beispiel für das Kommentieren der Name-Eigenschaft

Der folgende Beispielcode zeigt, wie sie die [Eigenschaft Name](name-property.md) des [**IAccessible-Objekts**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ein Steuerelement mithilfe der direkten Anmerkung ändern. Um die Dinge einfach zu halten, verwendet das Beispiel eine hart codierte Zeichenfolge ("Neuer Steuerelementname"), um die Name-Eigenschaft zu festlegen. Hart codierte Zeichenfolgen sollten in der endgültigen Version Ihrer Anwendung nicht verwendet werden, da sie nicht lokalisiert werden können. Laden Sie stattdessen immer Zeichenfolgen aus Ihrer Ressourcendatei. Außerdem zeigt das Beispiel nicht die Aufrufe der [Funktionen CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [CoUninitialize.](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[API für dynamische Anmerkungen](dynamic-annotation-api.md)
</dt> <dt>

[Bereitstellen der Name-Eigenschaft](providing-the-name-property.md)
</dt> <dt>

[Testtools](testing-tools.md)
</dt> </dl>

 

 