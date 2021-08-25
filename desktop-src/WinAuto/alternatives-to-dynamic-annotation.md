---
title: Alternativen zur dynamischen Anmerkung
description: Alternativen zur dynamischen Anmerkung
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af7582ec0fa3f317a0fabbdde0474c6a2e4d0b361062243d7518edf317477ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122430"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternativen zur dynamischen Anmerkung

Es gibt andere Möglichkeiten, benutzerdefinierte [**IAccessible-Unterstützung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für Benutzeroberflächenelemente zu bieten, und in einigen Fällen sind sie die richtige Lösung. Vor der dynamischen Anmerkung waren diese alternativen Techniken die einzigen Optionen, die Entwicklern zur Verfügung stehen. Dazu gehören die Implementierung aller **IAccessible-Schnittstellen** und programmgesteuerten Techniken.

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementieren der IAccessible-Schnittstelle

Eine alternative Methode ist die Implementierung der [**IAccessible-Schnittstelle.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Dieser Ansatz ist häufig für benutzerdefinierte Steuerelemente oder grundlegend unterschiedliche Benutzeroberflächenelemente erforderlich. Die Entwicklungs- und Testkosten sind jedoch so signifikant, dass sie vermieden werden sollten, es sei denn, dies ist wirklich erforderlich. Wenn es das Ziel ist, eine einzelne Eigenschaft zu ändern, sind die Kosten schwierig zu rechtfertigen.

## <a name="programmatic-techniques"></a>Programmgesteuerte Techniken

Eine weitere Möglichkeit besteht in der Verwendung von Unterklassen- und Umbruchtechniken, um die Informationen zu ändern, die für eine bestimmte Eigenschaft verfügbar gemacht werden. Dies ist die Technik, die die dynamische Anmerkung ersetzen soll. Um eine einzelne Eigenschaft mithilfe von Unterklassen und Wrapping zu überschreiben, muss der Entwickler die folgenden Schritte ausführen:

1.  Unterklasse des HWND des [**IAccessible-Objekts.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
2.  Fangen Sie [**die WM \_ GETOBJECT-Nachricht**](wm-getobject.md) für den richtigen IParam/OBJID-Wert ab.
3.  Senden Sie [**die WM \_ GETOBJECT-Nachricht**](wm-getobject.md) mithilfe der [*CallWndProc-Funktion*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) an die Basisklasse. Wenn null zurückgegeben wird, rufen Sie [**CreateStdAccessibleObject auf.**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) Rufen Sie [**andernfalls LresultFromObject für**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) den zurückgegebenen Wert auf, um den nativen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Steuerelements zu erhalten.
4.  Erstellen Sie eine Wrapperklasse, die [**IAccessible implementiert**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und den **IAccessible-Schnittstellenzeiger** umschließt, der im vorherigen Schritt zurückgegeben wurde. Diese Wrapperklasse sendet alle Methoden  und Eigenschaften an den ursprünglichen IAccessible-Schnittstellenzeiger, mit Ausnahme der Methoden, die überschrieben werden sollen. Dies umfasst das Schreiben von Weiterleitungscode für alle 21 Eigenschaften und Methoden der **IAccessible-Schnittstelle,** unabhängig davon, wie viele tatsächlich überschrieben werden.

Außerdem müssen Entwickler die folgenden Bedingungen überprüfen:

-   Die überschriebene Methode oder Eigenschaft darf nur die erforderlichen untergeordneten [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) IDs verarbeiten und alle anderen an den ursprünglichen IAccessible-Schnittstellenzeiger weitergeleitet werden.
-   Wrapping darf [**IEnumVARIANT-**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) und [**IOleWindow-Schnittstellen**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) nur dann weiterverenden, wenn sie vom ursprünglichen Objekt unterstützt werden.
-   Die Verweiszählung muss ordnungsgemäß verarbeitet werden, insbesondere, wenn andere Schnittstellen unterstützt werden.
-   [**IDispatch-Rückgabewerte**](idispatch-interface.md) müssen ordnungsgemäß behandelt werden, insbesondere mit der [**ITypeInfo::Invoke-Methode,**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) die mit einem Schnittstellenzeiger auf die Wrapperschnittstelle und nicht mit einem Zeiger auf die ursprüngliche [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aufgerufen werden muss.

Diese Techniken erfordern viel Arbeit, auch wenn nur eine oder zwei Eigenschaften überschrieben werden müssen. Der Großteil des resultierenden Codes betrifft Unterklassen und Umbrüche, und nur ein kleiner Bruchteil stellt tatsächlich die überschriebenen Informationen zur Verfügung.

Es gibt jedoch Szenarien, in denen diese Techniken erforderlich sind. Wenn Sie z. B. strukturelle Änderungen vornehmen, um ein Platzhalter-Benutzeroberflächenelement zu erstellen, sollten Sie diese Techniken anstelle der dynamischen Anmerkung verwenden.

## <a name="fixing-names-derived-from-labels"></a>Korrigieren von Namen, die von Bezeichnungen abgeleitet wurden

Einige allgemeine Microsoft Win32-Steuerelemente, z. B. das Bearbeitungsfeld-Steuerelement, werden fast immer mit einer Bezeichnung (einem LTEXT-Eintrag in der Ressourcendatei) oder einem Gruppenfeld (GROUPBOX in der Ressourcendatei) verwendet. Microsoft Active Accessibility die Name-Eigenschaft des Steuerelements automatisch von seiner Bezeichnung ab. Bei solchen Steuerelementen wird der Fenstertext (in Microsoft Visual Studio als Name- oder ID-Eigenschaft dargestellt) ignoriert, da er in der Regel automatisch generiert und selten sehr beschreibend ist. Beispiel: "IDC \_ EDIT1".

Wenn die Benutzeroberfläche der Anwendung nicht ordnungsgemäß entworfen wurde, Microsoft Active Accessibility den Namen möglicherweise nicht richtig festlegen. Um einem Steuerelement zugeordnet zu werden, muss die Bezeichnung oder das Gruppenfeld unmittelbar vor dem dynamischen Steuerelement in der Registerkarten reihenfolge platziert werden.

Die Reihenfolge der Registerkarten kann mithilfe des Tools in Visual Studio (im **Menü Format,** wenn der Ressourcen-Editor geöffnet ist) oder durch direktes Bearbeiten der Ressourcendatei geändert werden.

Das folgende Beispiel zeigt die Beschreibung einer Ressourcendatei eines Dialogfelds, das zwei beschriftete Bearbeitungsfelder enthält.


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



In diesem Beispiel werden die Bezeichnungen und Steuerelemente nicht in der richtigen Reihenfolge aufgeführt. Daher weist Microsoft Active Accessibility dem Bearbeitungsfeld für Vornamen den Namen "Nachname" und dem Bearbeitungsfeld "Nachname" überhaupt keinen Namen zu.

Das folgende Beispiel zeigt die richtige Ressourcenauflistung. Beachten Sie auch, dass Tastenkombinationen in den Bezeichnungen festgelegt wurden.


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



Wenn Steuerelemente über ergänzende Bezeichnungen verfügen, z. B. für Mindest- und Höchstwerte auf einer Trackleiste, sollten diese Bezeichnungen nach dem Steuerelement in der Reihenfolge der Registerkarten platziert werden. Die Hauptbezeichnung des Steuerelements muss unmittelbar vor dem Steuerelement selbst angezeigt werden.

## <a name="naming-controls-without-labels"></a>Benennen von Steuerelementen ohne Bezeichnungen

Es ist nicht immer möglich oder wünschenswert, für jedes Steuerelement eine sichtbare Bezeichnung zu haben. Sie können jedoch weiterhin einen Namen für das Steuerelement angeben, indem Sie eine unsichtbare Bezeichnung hinzufügen. Wie immer muss die unsichtbare Bezeichnung dem Steuerelement in der Registerkartenfolge unmittelbar vorangeordnet sein.

Wenn Sie den Ressourcen-Editor in Microsoft Visual Studio .NET verwenden, können Sie die Visible-Eigenschaft auf False festlegen. Um die Bezeichnung beim Bearbeiten der Ressourcendatei (.rc) unsichtbar zu machen, fügen Sie NOT WS VISIBLE oder dem Stilteil des Bezeichnungssteuerzeichen-Steuerelements hinzu, wie im folgenden \_ Beispiel gezeigt.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Beachten Sie, dass jede bestimmte Tastenkombination funktioniert, obwohl die Bezeichnung unsichtbar ist.

 

 