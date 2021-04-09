---
title: Sicherstellen, dass Benutzeroberflächen Elemente ordnungsgemäß benannt sind
description: In diesem Thema wird beschrieben, wie Sie die Namen der Benutzeroberflächen Elemente in Ihren Microsoft Win32-Anwendungen angeben, damit Microsoft Active Accessibility die Namen für Client Anwendungen mithilfe von "IAccessible \ 32;" korrekt verfügbar machen kann. Name-Eigenschaft.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948801"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>Sicherstellen, dass Benutzeroberflächen Elemente ordnungsgemäß benannt sind

In diesem Thema wird beschrieben, wie Sie die Namen der Benutzeroberflächen Elemente in Ihren Microsoft Win32-Anwendungen angeben, damit Microsoft Active Accessibility die Namen von Client Anwendungen mithilfe der Eigenschaft " [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name](name-property.md)" genau verfügbar machen kann.

Die Informationen in diesem Abschnitt gelten nur für Microsoft Active Accessibility. Dies gilt nicht für Anwendungen, die Microsoft UI Automation verwenden, oder für Anwendungen, die auf Markup Sprachen basieren, z. b. html, Dynamic HTML (DHTML) oder XML.

-   [Übersicht](#overview)
-   [Fehler durch falsche Benennung](#how-incorrect-naming-causes-problems)
-   [Abrufen der Name-Eigenschaft durch MSAA](#how-msaa-gets-the-name-property)
-   [Suchen und Beheben von Benennungs Problemen](#how-to-find-and-correct-naming-problems)
-   [So benennen Sie eine TrackBar ordnungsgemäß](#how-to-correctly-name-a-trackbar)
-   [Verwenden von nicht sichtbaren Bezeichnungen zum Benennen von Steuerelementen](#how-to-use-invisible-labels-to-name-controls)
-   [Verwenden der direkten Anmerkung zum Angeben der Name-Eigenschaft](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Schritte zum Hinzufügen einer Anmerkung zu der Name-Eigenschaft](#steps-for-annotating-the-name-property)
    -   [Beispiel für das kommentieren der Name-Eigenschaft](#example-of-annotating-the-name-property)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

In Microsoft Active Accessibility wird jedes Benutzeroberflächen Element in einer Anwendung durch ein Objekt dargestellt, das die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle verfügbar macht. Client Anwendungen verwenden die Eigenschaften und Methoden der **IAccessible** -Schnittstelle für die Interaktion mit dem UI-Element und das Abrufen von Informationen über die Schnittstelle. Eine der wichtigsten Eigenschaften, die von der **IAccessible** -Schnittstelle verfügbar gemacht wird, ist die [Name-Eigenschaft](name-property.md). Client Anwendungen verlassen sich auf die Name-Eigenschaft, um dem Benutzer ein Benutzeroberflächen Element zu suchen, zu identifizieren oder zu ankündigen. Wenn die Name-Eigenschaft eines bestimmten UI-Elements von Microsoft Active Accessibility nicht ordnungsgemäß verfügbar gemacht werden kann, ist es nicht möglich, dass Client Anwendungen dieses UI-Element dem Benutzer präsentieren, und das Benutzeroberflächen Element ist für Benutzer mit Behinderungen nicht zugänglich.

## <a name="how-incorrect-naming-causes-problems"></a>Fehler durch falsche Benennung

Zum Veranschaulichen der Probleme, die durch eine falsche Benennung von UI-Elementen verursacht werden, sollten Sie das in der folgenden Abbildung gezeigte namens Eingabeformular in Erwägung gezogen.

![Darstellung eines einfachen Formulars für die Eingabe von vor-und Nachname](images/incorrect-form.png)

Obwohl die Benutzeroberflächen Elemente im Formular okay aussehen, ist die programmgesteuerte Implementierung falsch. An einen Microsoft Active Accessibility-Client, z. b. eine Bildschirm Sprachausgabe, lautet die [Name-Eigenschaft](name-property.md) des Top-Bearbeitungs Steuer Elements "Nachname:&quot;, und die Name-Eigenschaft des unteren Bearbeitungs Steuer Elements ist eine leere Zeichenfolge (&quot;"). Die Sprachausgabe liest das oberste Bearbeitungs Steuerelement als "Nachname", obwohl der Benutzer erwartet, dass der Vorname den Vornamen erhält. Die Sprachausgabe liest das zweite Bearbeitungs Steuerelement als "kein Name", sodass der Benutzer nicht weiß, was in das zweite Bearbeitungs Steuerelement eingetippt werden muss. Die Sprachausgabe kann den Benutzer nicht dazu unterstützen, Daten in diese einfache Form einzugeben.

Ein weiteres Problem mit dem Formular besteht darin, dass keinem der Bearbeitungs Steuerelemente Tastenkombinationen zugewiesen werden. Der Benutzer wird gezwungen, entweder die Tab-Taste zu den Steuerelementen zu bewegen oder die Maus zu verwenden.

In den folgenden Abschnitten wird die Quelle dieser Probleme erläutert und Richtlinien für deren Behebung bereitgestellt.

## <a name="how-msaa-gets-the-name-property"></a>Abrufen der Name-Eigenschaft durch MSAA

Die [Name-Eigenschafts](name-property.md) Zeichenfolge wird von Microsoft Active Accessibility abhängig vom Typ des Benutzeroberflächen Elements von verschiedenen Speicherorten abgerufen. Für die meisten Elemente der Benutzeroberfläche, denen Fenster Text zugeordnet ist, verwendet Microsoft Active Accessibility den Fenster Text als Name-Eigenschafts Zeichenfolge. Beispiele für diese Art von Benutzeroberflächen Element sind Steuerelemente wie Schaltflächen, Menü Elemente und Quick Infos.

Bei den folgenden Steuerelementen ignoriert Microsoft Active Accessibility den Fenster Text und sucht stattdessen nach einer statischen Text Bezeichnung (oder Gruppenfeld Bezeichnung), die dem Steuerelement in der Aktivier Reihenfolge unmittelbar vorangestellt ist.

-   Kombinations Felder
-   Datums-und Uhrzeit-Picker
-   Bearbeiten und Rich Edit-Steuerelemente
-   IP-Adress Steuerelemente
-   Listenfelder
-   Auflisten von Ansichten
-   Status anzeigen
-   Bild Lauf leisten
-   Statische Steuerelemente, die das SS- \_ Symbol oder den SS- \_ bitmapstil aufweisen
-   Trackbars
-   Struktur Ansichten

Wenn die vorangehenden Steuerelemente nicht von statischen Text Bezeichnungen begleitet werden oder die Bezeichnungen nicht ordnungsgemäß implementiert sind, kann Microsoft Active Accessibility nicht die richtige [Name-Eigenschaft](name-property.md) für Client Anwendungen bereitstellen.

Den meisten vorangehenden Steuerelementen ist tatsächlich ein Fenster Text zugeordnet. Der Ressourcen-Editor generiert automatisch den Fenster Text, der aus einer generischen Zeichenfolge wie z. b. "Edit1" oder "listbox3" besteht. Obwohl Entwickler den generierten Fenster Text durch sinnvolleren Text ersetzen können, werden die meisten nie durchgeführt. Da der generierte Fenster Text für den Benutzer keine Bedeutung hat, wird er von Microsoft Active Accessibility ignoriert und stattdessen die zugehörige statische Text Bezeichnung verwendet.

## <a name="how-to-find-and-correct-naming-problems"></a>Suchen und Beheben von Benennungs Problemen

In dem namens Eingabeformular, das unter wie falsche Benennung Probleme verursacht, besteht die Ursache der Probleme darin, dass die Aktivier Reihenfolge der Steuerelemente falsch ist. Wenn Sie die Benutzeroberfläche mit einem Testtool wie " [überprüfen"](inspect-objects.md) untersuchen, werden die Probleme mit der Objekthierarchie angezeigt. Der folgende Screenshot zeigt die beschädigte Objekthierarchie des Namens Eingabeformulars, wie Sie in überprüfen angezeigt wird.

![Screenshot des Überprüfungs Tools, das eine fehlerhafte Objekthierarchie des Namens Eingabeformulars anzeigt](images/incorrect-object-hierarchy.png)

Beachten Sie im vorherigen Screenshot, dass die Objekthierarchie nicht mit der Struktur der Steuerelemente identisch ist, wie Sie in der Benutzeroberfläche des Namens Eingabeformulars angezeigt werden. Beachten Sie auch [, dass die Überprüfung](inspect-objects.md) dem nächsten Element den falschen Namen zugewiesen hat (das Bearbeitungs Steuerelement zum Eingeben des Vornamen und sollte ein benannter Vorname sein). Beachten Sie schließlich, dass untersuchen keinen Namen für das letzte Element finden konnte (es ist das Bearbeitungs Steuerelement zum Eingeben des Nachnamen und sollte den Namen "Nachname:" aufweisen).

Das folgende Beispiel zeigt den Inhalt der Ressourcen Datei für das namens Eingabeformular. Beachten Sie, dass die Aktivier Reihenfolge nicht mit der logischen Struktur der Steuerelemente übereinstimmt, wie Sie in der Benutzeroberfläche angezeigt werden. Beachten Sie auch, dass für die beiden Bearbeitungs Steuerelemente keine Tastenkombinationen angegeben werden.

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

Zum Beheben der Probleme mit dem namens Eingabeformular sollte die Ressourcen Datei (. RC) bearbeitet werden, um Tastenkombinationen anzugeben, und die Steuerelemente müssen in der folgenden Reihenfolge platziert werden:

1.  Die statische Text Bezeichnung "&First Name:".
2.  Das Bearbeitungs Steuerelement für die Eingabe des Vornamen (IDC \_ Edit1).
3.  Die statische Text Bezeichnung "&Nachname:".
4.  Das Bearbeitungs Steuerelement für die Eingabe des Nachnamen (IDC \_ Edit2).
5.  Die Standard-Schaltfläche "OK".

Das folgende Beispiel zeigt die korrigierte Ressourcen Datei für das namens Eingabeformular:

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

Wenn Sie Korrekturen an einer Ressourcen Datei vornehmen möchten, können Sie entweder die Datei direkt bearbeiten, oder Sie können das Tab-Reihen folgen Tool in Microsoft Visual Studio verwenden. Sie können auf das Registerkarten-Bestell Tool in Visual Studio zugreifen, indem Sie entweder STRG + D drücken, oder indem Sie im Menü **Format** die Option **Tab-Reihenfolge** auswählen.

Nachdem Sie die Anwendung korrigiert und neu erstellt haben, sieht die Benutzeroberfläche des Namens Eintrags Formulars wie zuvor aus. Allerdings werden von Microsoft Active Accessibility jetzt die richtigen namens Eigenschaften für Client Anwendungen bereitgestellt, und der Fokus wird ordnungsgemäß festgelegt, wenn der Benutzer die Tastenkombinationen ALT + F oder ALT + L drückt. Über [prüfen](inspect-objects.md) wird außerdem die richtige Objekthierarchie angezeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des Tools des zugänglichen Explorers, das eine korrekte Objekthierarchie des Namens Eingabeformulars anzeigt](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>So benennen Sie eine TrackBar ordnungsgemäß

Stellen Sie beim Definieren einer TrackBar (oder eines Schiebereglers) sicher, dass die statische Haupt Bezeichnung für die TrackBar vor der TrackBar angezeigt wird und dass die statischen Text Bezeichnungen für die minimalen und maximalen Bereiche nach der TrackBar angezeigt werden. Beachten Sie, dass Microsoft Active Accessibility die statische Text Bezeichnung verwendet, die direkt einem Steuerelement als [Name-Eigenschaft](name-property.md) für das Steuerelement vorangestellt ist. Wenn Sie die statische Haupt Bezeichnung direkt vor der TrackBar und die anderen Bezeichnungen danach platzieren, wird sichergestellt, dass Microsoft Active Accessibility die richtige Namenseigenschaft für einen Client bereitstellt.

Die folgende Abbildung zeigt eine typische TrackBar mit einer statischen Haupt Bezeichnung namens "Geschwindigkeit" und statische Text Bezeichnungen für die minimalen ("min") und maximalen ("maximalen") Bereiche.

![Abbildung eines TrackBar-Steuer Elements, das über eine Haupt Bezeichnung und Bezeichnungen für die minimalen und maximalen Bereiche verfügt](images/speed-trackbar.png)

Das folgende Beispiel zeigt die korrekte Methode zum Definieren einer TrackBar und ihrer statischen Text Bezeichnungen in der Ressourcen Datei:

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

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Verwenden von nicht sichtbaren Bezeichnungen zum Benennen von Steuerelementen

Es ist nicht immer möglich oder wünschenswert, dass für jedes Steuerelement eine sichtbare Bezeichnung vorhanden ist. Beispielsweise kann es vorkommen, dass das Hinzufügen von Bezeichnungen unerwünschte Änderungen an der Darstellung der Benutzeroberfläche verursachen kann. In diesem Fall können Sie unsichtbare Bezeichnungen verwenden. Microsoft Active Accessibility nimmt weiterhin den Text an, der einer unsichtbaren Bezeichnung zugeordnet ist, aber die Bezeichnung wird nicht in der visuellen Benutzeroberfläche angezeigt, oder Sie wird nicht beeinträchtigt.

Wie bei sichtbaren Bezeichnungen muss dem Steuerelement in der Aktivier Reihenfolge unmittelbar eine unsichtbare Bezeichnung vorangestellt werden. Um eine Bezeichnung in einer Ressourcen Datei (. RC) unsichtbar zu machen, fügen Sie `NOT WS_VISIBLE` oder dem Formatvorlagen `|~WS_VISIBLE` Teil des statischen Text-Steuer Elements hinzu. Wenn Sie den Ressourcen-Editor in Visual Studio verwenden, können Sie die Visible-Eigenschaft auf false festlegen.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Verwenden der direkten Anmerkung zum Angeben der Name-Eigenschaft

Die Standard Proxys, die in der Komponente Microsoft Active Accessibility Runtime enthalten sind, stellen Oleacc.dll automatisch ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für alle standardmäßigen Windows-Steuerelemente bereit. Wenn Sie ein standardmäßiges Windows-Steuerelement anpassen, sind die Standard Proxys am besten geeignet, um alle **IAccessible** -Eigenschaften für Ihr benutzerdefiniertes Steuerelement genau bereitzustellen. Sie sollten ein angepasstes Steuerelement gründlich testen, um sicherzustellen, dass die Standardproxys exakte und vollständige Eigenschaftswerte Wenn beim Testen falsche oder unvollständige Eigenschaftswerte angezeigt werden, können Sie die dynamische Anmerkung-Technik mit der Bezeichnung "direkte Anmerkung" verwenden, um korrekte Eigenschaftswerte bereitzustellen und fehlende Werte hinzuzufügen.

Beachten Sie, dass die dynamische Anmerkung nicht nur für Steuerelemente bestimmt ist, die von den Microsoft-Active Accessibility Proxys Sie können es auch verwenden, um Eigenschaften für ein beliebiges Steuerelement zu ändern oder anzugeben, das seine eigene [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung bereitstellt.

Dieser Abschnitt konzentriert sich auf die Verwendung der direkten Anmerkung, um einen korrekten Wert für die [Name-Eigenschaft](name-property.md) des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts für ein Steuerelement bereitzustellen. Mit der direkten Anmerkung können auch andere Eigenschaftswerte bereitgestellt werden. Außerdem sind andere dynamische Anmerkung-Techniken neben direkter Anmerkung verfügbar, und die Features und Funktionen der API für dynamische Anmerkungen werden weit über die in diesem Abschnitt beschriebenen Funktionen hinaus erweitert. Weitere Informationen zur dynamischen Anmerkung finden Sie unter [Dynamic Annotation-API](dynamic-annotation-api.md).

### <a name="steps-for-annotating-the-name-property"></a>Schritte zum Hinzufügen einer Anmerkung zu der Name-Eigenschaft

Die Verwendung der direkten Anmerkung zum Ändern der [Name-Eigenschaft](name-property.md) eines Steuer Elements umfasst die folgenden Schritte.

1.  Fügen Sie die folgenden Header Dateien ein:
    -   Initguid. h
    -   Oleacc. h

    > [!Note]  
    > Zum Definieren von GUIDs müssen Sie Initguid. h vor Oleacc. h in dieselbe Datei einschließen.

     

2.  Initialisieren Sie die Component Object Model (com)-Bibliothek, indem Sie die [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion aufrufen, in der Regel während des Anwendungs Initialisierungs Prozesses.
3.  Nachdem das Ziel Steuerelement erstellt wurde (in der Regel während der " [WM \_ InitDialog](../dlgbox/wm-initdialog.md) "-Meldung), erstellen Sie eine Instanz des Anmerkung-Managers und rufen einen Zeiger auf den [**zugehörigen IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Zeiger ab.
4.  Kommentieren Sie die [Name-Eigenschaft](name-property.md) des Ziel Steuer Elements mit der [**IAccPropServices::**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) ""-Methode.

5.  Geben Sie den [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Zeiger frei.
6.  Bevor das Ziel Steuerelement zerstört wird (in der Regel bei der Behandlung der WM-Lösch Nachricht), erstellen Sie eine Instanz des Anmerkung-Managers, und rufen Sie einen Zeiger auf seine [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Schnittstelle ab. [ \_](../winmsg/wm-destroy.md)
7.  Verwenden Sie die [**IAccPropServices:: clearhwnddie**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) -Methode, um die [Name-Eigenschafts](name-property.md) Anmerkungen aus dem Ziel Steuerelement zu löschen.
8.  Geben Sie den [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Zeiger frei.
9.  Bevor die Anwendung beendet wird (in der Regel bei der Verarbeitung der WM-Lösch Nachricht), müssen Sie die com-Bibliothek freigeben, indem Sie die Funktion " [count](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) " aufrufen [ \_ ](../winmsg/wm-destroy.md)

Die [**IAccPropServices::-Funktion der Funktion "IAccPropServices::**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) " erfordert fünf Parameter. Die ersten drei –*HWND*, *idobject* und *idchild*– werden kombiniert, um das Steuerelement zu identifizieren. Der vierte Parameter, *idProp*, gibt den Bezeichner der Eigenschaft an, die geändert werden soll. Um die [Name-Eigenschaft](name-property.md)zu ändern, legen Sie *idProp* auf den **\_ \_ Namen des PROPID-ACC** fest. (Eine Liste mit anderen Eigenschaften, die Sie über die direkte Anmerkung festlegen können, finden Sie unter [Verwenden der direkten](using-direct-annotation.md)Anmerkung.) Der letzte Parameter von " **ssthwndpropstr**, *Str*" ist die neue Zeichenfolge, die als "Name"-Eigenschaft verwendet werden soll.

### <a name="example-of-annotating-the-name-property"></a>Beispiel für das kommentieren der Name-Eigenschaft

Der folgende Beispielcode zeigt, wie Sie mit der direkten Anmerkung die [Name-Eigenschaft](name-property.md) des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts für ein-Steuerelement ändern können. Um dies zu gewährleisten, wird im Beispiel eine hart codierte Zeichenfolge ("neuer Steuerelement Name") verwendet, um die Name-Eigenschaft festzulegen. Hart codierte Zeichen folgen sollten nicht in der endgültigen Version der Anwendung verwendet werden, da Sie nicht lokalisiert werden können. Laden Sie stattdessen Zeichen folgen immer aus der Ressourcen Datei. Das Beispiel zeigt auch nicht die Aufrufe der Funktionen [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [zählinitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


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

**Licher**
</dt> <dt>

[Dynamic-Annotation-API](dynamic-annotation-api.md)
</dt> <dt>

[Bereitstellen der Name-Eigenschaft](providing-the-name-property.md)
</dt> <dt>

[TestTools](testing-tools.md)
</dt> </dl>

 

 