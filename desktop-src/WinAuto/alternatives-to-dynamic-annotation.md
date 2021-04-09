---
title: Alternativen zu dynamischer Anmerkung
description: Alternativen zu dynamischer Anmerkung
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101883"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternativen zu dynamischer Anmerkung

Es gibt weitere Möglichkeiten, angepasste [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung für Benutzeroberflächen Elemente bereitzustellen, und in einigen Fällen sind Sie die richtige Lösung. Vor der dynamischen Anmerkung waren diese alternativen Techniken die einzigen Optionen, die Entwicklern zur Verfügung standen. Dazu gehört das Implementieren der gesamten **IAccessible** -Schnittstelle und der programmgesteuerten Techniken.

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementieren der gesamten IAccessible-Schnittstelle

Eine alternative Methode besteht darin, die gesamte [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle zu implementieren. Diese Vorgehensweise ist häufig für benutzerdefinierte Steuerelemente oder völlig unterschiedliche Elemente der Benutzeroberfläche erforderlich. die Entwicklungs-und Testkosten sind jedoch so groß, dass Sie nur vermieden werden sollten, wenn es wirklich notwendig ist. Wenn das Ziel darin besteht, eine einzelne Eigenschaft zu ändern, ist es schwierig, die Kosten zu rechtfertigen.

## <a name="programmatic-techniques"></a>Programmgesteuerte Techniken

Eine andere Möglichkeit besteht darin, die Informationen, die für eine bestimmte Eigenschaft verfügbar gemacht werden, mithilfe von Unterklassen und Wrapping Techniken zu ändern. Dies ist die Technik, die durch die dynamische Anmerkung ersetzt werden soll. Um eine einzelne Eigenschaft mithilfe von Unterklassen und Wrapping zu überschreiben, muss der Entwickler die folgenden Schritte ausführen:

1.  Unterklasse das HWND des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts.
2.  Fangen Sie die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht für den korrekten IParam/objID-Wert ab.
3.  Leiten Sie die [**WM \_ GetObject**](wm-getobject.md) -Nachricht mithilfe der [*callwndproc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) -Funktion an die Basisklasse weiter. Wenn 0 (null) zurückgegeben wird, aufrufen Sie " [**foratestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); Rufen Sie andernfalls [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) für den zurückgegebenen Wert auf, um den nativen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger des Steuer Elements abzurufen.
4.  Erstellen Sie eine Wrapper Klasse, die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert und den **IAccessible** -Schnittstellen Zeiger umschließt, der aus dem vorherigen Schritt zurückgegeben wurde. Diese Wrapper Klasse sendet alle Methoden und Eigenschaften an den ursprünglichen **IAccessible** -Schnittstellen Zeiger, mit Ausnahme derjenigen, die überschrieben werden sollen. Dies umfasst das Schreiben von Weiterleitungs Code für alle 21 Eigenschaften und Methoden der **IAccessible** -Schnittstelle, unabhängig davon, wie viele tatsächlich überschrieben werden.

Außerdem müssen Entwickler die folgenden Bedingungen überprüfen:

-   Die überschriebene Methode oder Eigenschaft darf nur die erforderlichen untergeordneten IDs verarbeiten und alle anderen an den ursprünglichen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger weiterleiten.
-   Beim umwickeln müssen auch [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) -und [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) -Schnittstellen weiterleiten, wenn Sie vom ursprünglichen Objekt unterstützt werden.
-   Die Verweis Zählung muss korrekt gehandhabt werden, insbesondere, wenn andere Schnittstellen unterstützt werden.
-   [**IDispatch**](idispatch-interface.md) -Rückgabewerte müssen ordnungsgemäß behandelt werden, insbesondere bei der [**ITypeInfo:: Aufrufen**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) -Methode, die mit einem Schnittstellen Zeiger auf die Wrapper Schnittstelle aufgerufen werden muss, nicht mit einem Zeiger auf die ursprüngliche [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle.

Diese Techniken erfordern eine beträchtliche Menge an Arbeit, auch wenn nur eine oder zwei Eigenschaften überschrieben werden müssen. Der Großteil des resultierenden Codes beschäftigt sich mit dem Unterklassen-und Wrapping Vorgang, und nur ein kleiner Bruchteil bietet tatsächlich die überschriebenen Informationen an.

Es gibt jedoch Szenarios, in denen diese Techniken benötigt werden. Wenn Sie z. b. strukturelle Änderungen vornehmen, um ein Platzhalter-Benutzeroberflächen Element zu erstellen, sollten Sie diese Techniken anstelle der dynamischen Anmerkung verwenden.

## <a name="fixing-names-derived-from-labels"></a>Von Bezeichnungen abgeleitete Namen werden repariert.

Einige allgemeine Microsoft Win32-Steuerelemente, wie z. b. das Bearbeitungsfeld-Steuerelement, werden fast immer mit einer Bezeichnung (einem LTEXT-Eintrag in der Ressourcen Datei) oder einem Gruppenfeld (GroupBox in der Ressourcen Datei) verwendet. Die Name-Eigenschaft des Steuer Elements wird von Microsoft Active Accessibility automatisch von der Bezeichnung abgeleitet. Bei solchen Steuerelementen wird der Fenster Text (in Microsoft Visual Studio als Name oder ID-Eigenschaft angezeigt) ignoriert, da er in der Regel automatisch generiert und selten sehr beschreibend ist. Beispiel: "IDC \_ Edit1".

Wenn die Benutzeroberfläche der Anwendung nicht ordnungsgemäß entworfen wurde, kann Microsoft Active Accessibility den Namen möglicherweise nicht ordnungsgemäß festlegen. Um einem-Steuerelement zugeordnet zu werden, muss die Bezeichnung oder das Gruppenfeld direkt vor dem dynamischen Steuerelement in der Aktivier Reihenfolge platziert werden.

Die Aktivier Reihenfolge kann geändert werden, indem Sie das Tool in Visual Studio verwenden (im Menü **Format** , wenn der Ressourcen-Editor geöffnet ist), oder indem Sie die Ressourcen Datei direkt bearbeiten.

Das folgende Beispiel zeigt die Beschreibung eines Dialog Felds einer Ressourcen Datei, das zwei beschriftete Bearbeitungsfelder enthält.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



In diesem Beispiel werden die Bezeichnungen und Steuerelemente nicht in der richtigen Aktivier Reihenfolge aufgelistet. Demzufolge weist Microsoft Active Accessibility den Namen "Nachname" dem Eingabefeld "First-Name" und dem Bearbeitungsfeld "Last Name" überhaupt keinen Namen zu.

Das folgende Beispiel zeigt die richtige Ressourcen Auflistung. Beachten Sie auch, dass die Tastenkombination in den Bezeichnungen festgelegt wurde.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



Wenn Steuerelemente über ergänzende Bezeichnungen verfügen, z. b. für Mindest-und Höchstwerte auf einer TrackBar, sollten diese Bezeichnungen nach dem-Steuerelement in der Aktivier Reihenfolge platziert werden. Die Haupt Bezeichnung des Steuer Elements muss direkt vor dem Steuerelement selbst angezeigt werden.

## <a name="naming-controls-without-labels"></a>Benennen von Steuerelementen ohne Bezeichnungen

Es ist nicht immer möglich oder wünschenswert, dass für jedes Steuerelement eine sichtbare Bezeichnung vorhanden ist. Sie können jedoch weiterhin einen Namen für das Steuerelement angeben, indem Sie eine unsichtbare Bezeichnung hinzufügen. Wie immer muss die unsichtbare Bezeichnung unmittelbar vor dem-Steuerelement in der Aktivier Reihenfolge stehen.

Wenn Sie den Ressourcen-Editor in Microsoft Visual Studio .NET verwenden, können Sie die Visible-Eigenschaft auf false festlegen. Um die Bezeichnung beim Bearbeiten der Ressourcen Datei (RC) unsichtbar zu machen, fügen Sie Not WS \_ Visible oder den Formatvorlagen Teil des Label-Steuer Elements hinzu, wie im folgenden Beispiel gezeigt.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Beachten Sie, dass alle festgelegten Tastenkombinationen funktionieren, auch wenn die Bezeichnung unsichtbar ist.

 

 