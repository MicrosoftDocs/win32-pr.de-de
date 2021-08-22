---
title: Verwendung untergeordneter IDs in Parametern
description: In diesem Thema werden Eingabeparameter, Ausgabeparameter und Sonderfälle zum Interpretieren von untergeordneten IDs beschrieben, die von IAccessible-Methoden zurückgegeben werden.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc0c3be970fb4a688a0a5447b72719428e78e074cbc7a17f2b6b698fcca177f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052720"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Verwendung untergeordneter IDs in Parametern

In diesem Thema werden Eingabeparameter, Ausgabeparameter und Sonderfälle zum Interpretieren von untergeordneten IDs beschrieben, die von [**IAccessible-Methoden zurückgegeben**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) werden.

## <a name="input-parameters"></a>Eingabeparameter

Viele der Microsoft Active Accessibility und die meisten [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nehmen eine [**VARIANT-Struktur**](/windows/win32/api/oaidl/ns-oaidl-variant) als Eingabeparameter an. Bei den meisten **IAccessible-Eigenschaften** können Cliententwickler mit diesem Parameter angeben, ob sie Informationen zum Objekt selbst oder zu einem der einfachen Elemente des Objekts wünschen.

Microsoft Active Accessibility stellt die Konstante **CHILDID \_ SELF** zur Verfügung, um anzugeben, dass Informationen über das Objekt selbst benötigt werden. Um Informationen zu einem einfachen Element zu erhalten, geben Cliententwickler die untergeordnete ID im [**VARIANT-Parameter**](/windows/win32/api/oaidl/ns-oaidl-variant) an.

Stellen Sie beim Initialisieren eines [**VARIANT-Parameters**](/windows/win32/api/oaidl/ns-oaidl-variant) sicher, dass Sie **VT \_ I4** im **vt-Member** zusätzlich zur Angabe des untergeordneten ID-Werts (oder **CHILDID \_ SELF)** im **lVal-Member** angeben.

Um beispielsweise den Namen eines Objekts und nicht eines der untergeordneten Elemente [](/windows/win32/api/oaidl/ns-oaidl-variant) des Objekts zu erhalten, initialisieren Sie variant für den ersten Parameter von [**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ SELF** im **lVal-Member** und **VT \_ I4** im **vt-Member),** und rufen Sie dann **IAccessible::get \_ accName auf.**

## <a name="output-parameters"></a>Ausgabeparameter

Mehrere [**IAccessible-Funktionen**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden verfügen über einen VARIANT-Ausgabeparameter, der eine untergeordnete ID oder einen [](/windows/win32/api/oaidl/ns-oaidl-variant) \* [**IDispatch-Schnittstellenzeiger**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) auf ein untergeordnetes Objekt enthält. Es gibt verschiedene Schritte, die ein Client ausführen muss, je nachdem, ob er eine untergeordnete **VT \_ I4-ID** (einfaches Element) oder einen **IDispatch-Schnittstellenzeiger** mit **CHILDID \_ SELF** (vollständiges Objekt) erhält. Wenn Sie diese  Schritte ausführen, stellen Sie einen IAccessible-Schnittstellenzeiger und eine untergeordnete ID bereit, die es Clients ermöglichen, die **IAccessible-Methoden** und -Eigenschaften zu verwenden. Diese Schritte gelten für die [**Methoden IAccessible::accHitTest,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)und [**get \_ accSelection.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) Sie gelten auch für die [**Clientfunktionen AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)und [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

In der folgenden Tabelle sind das mögliche zurückgegebene Ergebnis und [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) die erforderlichen Schritte nach der Verarbeitung aufgeführt, damit Clients über einen IAccessible-Schnittstellenzeiger und eine untergeordnete ID verfügen.



| Zurückgegebenes Ergebnis                                      | Nachverarbeitung für den Rückgabewert                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDispatch-Schnittstellenzeiger**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Dies ist ein vollständiges -Objekt. Rufen [**Sie QueryInterface auf,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) um auf den [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zu zugreifen.<br/> Verwenden Sie den [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) mit **CHILDID \_ SELF, um** auf **IAccessible-Methoden** und -Eigenschaften zu zugreifen.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| Untergeordnete VT \_ I4-ID                                      | Rufen [**Sie IAccessible::get \_ accChild mithilfe**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) der untergeordneten ID auf, um zu sehen, ob Sie über einen [**IDispatch-Schnittstellenzeiger**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) verfügen. Wenn Sie einen [**IDispatch-Schnittstellenzeiger**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) erhalten, verwenden Sie ihn mit **CHILDID \_ SELF,** um auf [**IAccessible-Schnittstellenmethoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Eigenschaften zu zugreifen.<br/> Wenn der Aufruf von [**\_ accChild fehlschlägt,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) verfügen Sie über ein einfaches -Element. Verwenden Sie [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) den ursprünglichen IAccessible-Schnittstellenzeiger (den, den Sie in Ihrem Aufruf der oben genannten Methode oder Funktion verwendet haben) mit der untergeordneten **VT \_ I4-ID,** die der Aufruf zurückgegeben hat.<br/> |



 

Bevor Sie einen [**VARIANT-Parameter verwenden**](/windows/win32/api/oaidl/ns-oaidl-variant) können, müssen Sie ihn initialisieren, indem Sie die COM-Funktion [**(VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model) aufrufen. Wenn Sie mit der Struktur fertig sind, rufen [**Sie VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) auf, um den für diese VARIANT reservierten Arbeitsspeicher **frei zu geben.**

## <a name="special-cases"></a>Sonderfälle

Es gibt Ausnahmen von den Richtlinien in der obigen Tabelle, z. B. wenn von der [**IAccessible::accHitTest-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) eine untergeordnete ID zurückgegeben wird. Server müssen eine [**IDispatch-Schnittstelle**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) zurückgeben, wenn das untergeordnete Objekt ein barrierefreies Objekt ist. Wenn eine untergeordnete ID von **IAccessible::accHitTest** zurückgegeben wird, ist das untergeordnete Element ein einfaches Element.

Darüber hinaus gibt es Sonderfälle für [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Weitere Informationen finden Sie unter **IAccessible::accNavigate** und [Räumliche und logische Navigation.](spatial-and-logical-navigation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[IDispatch-Schnittstelle](idispatch-interface.md)
</dt> <dt>

[VARIANT-Struktur](variant-structure.md)
</dt> </dl>

 

