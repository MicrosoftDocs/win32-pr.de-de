---
title: Verwendung von untergeordneten IDs in Parametern
description: In diesem Thema werden Eingabeparameter, Ausgabeparameter und Sonderfälle für die Interpretation von untergeordneten IDs beschrieben, die von IAccessible-Methoden zurückgegeben werden
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03026e6abf769efab95cc513231fad3af64511f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390564"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Verwendung von untergeordneten IDs in Parametern

In diesem Thema werden Eingabeparameter, Ausgabeparameter und Sonderfälle für die Interpretation von untergeordneten IDs beschrieben, die von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden zurückgegeben werden

## <a name="input-parameters"></a>Eingabeparameter

Viele der Funktionen von Microsoft Active Accessibility und die meisten der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften nehmen eine [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur als Eingabeparameter an. Bei den meisten **IAccessible** -Eigenschaften können Client Entwickler mithilfe dieses Parameters angeben, ob Sie Informationen über das Objekt selbst oder über eines der einfachen Elemente des Objekts wünschen.

Microsoft Active Accessibility stellt die Konstante **childID \_ Self** bereit, um anzugeben, dass Informationen über das Objekt selbst benötigt werden. Zum Abrufen von Informationen über ein einfaches Element geben Client Entwickler die untergeordnete ID im [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Parameter an.

Wenn Sie einen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Parameter initialisieren, achten Sie darauf, dass Sie **VT \_ I4** im **VT** -Element zusätzlich zur Angabe des untergeordneten ID-Werts (oder **childID \_ Self**) im **LVAL** -Member angeben.

Um z. b. den Namen eines Objekts und nicht eines der untergeordneten Elemente des Objekts abzurufen, initialisieren Sie die [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) für den ersten Parameter von [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **childID \_ Self** im **LVAL** -Member und **VT \_ I4** im **VT** -Member), und nennen **Sie dann IAccessible:: get \_ accName**.

## <a name="output-parameters"></a>Ausgabeparameter

Mehrere [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Funktionen und-Methoden verfügen über einen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) - \* Ausgabeparameter, der eine untergeordnete ID oder einen [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger auf ein untergeordnetes Objekt enthält. Es gibt verschiedene Schritte, die ein Client ausführen muss, je nachdem, ob er eine **VT \_ I4** Child ID (einfaches Element) oder einen **IDispatch** -Schnittstellen Zeiger mit **childID \_ Self** (Full Object) empfängt. Durch die folgenden Schritte wird ein **ibarrierefreie** Schnittstellen Zeiger und eine untergeordnete ID bereitgestellt, die es Clients ermöglichen, die **IAccessible** -Methoden und-Eigenschaften zu verwenden. Diese Schritte gelten für die Methoden [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)und [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) . Sie gelten auch für die Client Funktionen [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)und [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

In der folgenden Tabelle werden die möglichen Ergebnisse und die erforderlichen nach Verarbeitungsschritte aufgelistet, damit Clients über einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger und eine untergeordnete ID verfügen.



| Ergebnis zurückgegeben                                      | Nachbearbeitung für den Rückgabewert                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger | Dabei handelt es sich um ein vollständiges Objekt. Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Zugriff auf den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger.<br/> Verwenden Sie den [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger mit **childID \_ Self** , um auf **IAccessible** -Methoden und-Eigenschaften zuzugreifen.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| VT \_ I4 untergeordnete ID                                      | Wenn Sie über einen [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger verfügen, wird [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) mithilfe der untergeordneten ID aufgerufen. Wenn Sie einen [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstellen Zeiger erhalten, verwenden Sie ihn mit **childID \_ Self** , um auf [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Schnittstellen Methoden und-Eigenschaften zuzugreifen.<br/> Wenn der get- [**\_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) -Rückruf fehlschlägt, haben Sie ein einfaches-Element. Verwenden Sie den ursprünglichen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger (den Sie in Ihrem Aufruf der oben erwähnten Methode oder Funktion verwendet haben) mit der untergeordneten **VT \_ I4** -ID, die der Aufruf zurückgegeben hat.<br/> |



 

Bevor Sie einen [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Parameter verwenden können, müssen Sie ihn initialisieren, indem Sie die [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) -Component Object Model (com)-Funktion aufrufen. Wenn Sie mit der Struktur fertig sind, können Sie [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) aufzurufen, um den für diese **Variante** reservierten Arbeitsspeicher freizugeben.

## <a name="special-cases"></a>Sonderfälle

Es gibt Ausnahmen zu den Richtlinien in der obigen Tabelle, z. b. Wenn eine untergeordnete ID von der [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) -Methode zurückgegeben wird. Server müssen eine [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Schnittstelle zurückgeben, wenn das untergeordnete Objekt ein Barrierefreies Objekt ist. Wenn eine untergeordnete ID von **IAccessible:: accHitTest** zurückgegeben wird, ist das untergeordnete Element ein einfaches Element.

Außerdem gibt es spezielle Fälle für die [**Zugriffs Navigation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Weitere Informationen finden Sie unter **IAccessible:: accNavigate** und [räumliche und logische Navigation](spatial-and-logical-navigation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[IDispatch-Schnittstelle](idispatch-interface.md)
</dt> <dt>

[VARIANT-Struktur](variant-structure.md)
</dt> </dl>

 

