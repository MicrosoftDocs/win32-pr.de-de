---
title: Verwenden der Server Anmerkung
description: Dieses Thema enthält Informationen zum Verwenden der Server Anmerkung zum Angeben eines Rückruf Objekts.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb545cd4dd016901d69f67d5ab5cab15dda08875
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341311"
---
# <a name="using-server-annotation"></a>Verwenden der Server Anmerkung

Dieses Thema enthält Informationen zum Verwenden der Server Anmerkung zum Angeben eines Rückruf Objekts.

**So überschreiben Sie eine Eigenschaft, die ein Rückruf Objekt angibt**

1.  Abrufen eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeigers auf das barrierefreie Element, das mit Anmerkungen versehen werden soll.
2.  Ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das barrierefreie Element auf, um einen [**iaccidentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) -Schnittstellen Zeiger zu erhalten.
3.  Rufen Sie [**iaccidentity:: getidentitystring ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) für den [**iaccidentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) -Schnittstellen Zeiger auf, um eine Zeichenfolge abzurufen, die das barrierefreie Element eindeutig identifiziert, das mit Anmerkungen versehen werden soll.
4.  Verwenden Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) zum Erstellen des [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) -Objekts.
5.  Erstellen Sie ein Component Object Model (com)-Objekt, das [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)implementiert.
6.  Rufen Sie [**IAccPropServices:: SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)auf, und übergeben Sie dabei die Identitäts Zeichenfolge, eine GUID, die die zu über schreibende Eigenschaft angibt, und einen Zeiger auf das [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) -Rückruf Objekt.
7.  Freigeben von Schnittstellen Zeigern und freiem Arbeitsspeicher.

Wenn ein Client die-Eigenschaft des barrierefreien Elements anfordert, wird das Rückruf Objekt aufgerufen, und der Wert wird an den Client zurückgegeben.

Wie beim Angeben eines Werts können Server Entwickler alternativ die [**IAccPropServices:: composehwndidentitystring**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) -Methode verwenden, um eine Identitäts Zeichenfolge abzurufen. oder Sie können die [**IAccPropServices:: Server**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) -Methode verwenden und die Parameter " *HWND*", " *idobject*" und " *idchild* " anstelle einer Identitäts Zeichenfolge angeben.

Bei Verwendung von [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) oder [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) für ein Container Objekt können Server Entwickler optional festlegen, dass die über schreibenden Informationen auch auf alle untergeordneten Elemente dieses Containers angewendet werden sollen.

Server können die Anmerkung jederzeit mithilfe von [**IAccPropServices:: Clear-**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops)Eigenschaften explizit löschen. Dies ist in der Regel nicht erforderlich, da der Anmerkung-Dienst Anmerkung-Informationen automatisch bereinigt und freigibt, wenn das barrierefreie Element, das mit Anmerkungen versehen wird, nicht mehr angezeigt wird.

Im folgenden finden Sie eine Liste der Eigenschaften, die mit dieser Prozedur kommentiert werden können.

## <a name="properties-supported-when-specifying-a-callback"></a>Unterstützte Eigenschaften beim Angeben eines Rückrufs

Beim Angeben eines Rückrufs können die folgenden Eigenschaften mit Anmerkungen versehen werden. Zurzeit können diese Eigenschaften nicht direkt mit Anmerkungen versehen werden, indem ein-Wert angegeben wird.



| Eigenschaft                      | type                                                             |
|-------------------------------|------------------------------------------------------------------|
| Name des PROPID- \_ ACC \_             | VT \_ BSTR                                                         |
| Beschreibung des PROPID- \_ ACC \_      | VT \_ BSTR                                                         |
| PROPID- \_ Rolle "ACC" \_             | VT \_ I4                                                           |
| Status des PROPID- \_ ACC \_            | VT \_ I4                                                           |
| PROPID \_ - \_ Hilfe zum ACC             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ KeyboardShortcut | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID- \_ ACC ( \_ ValueMap)         | VT \_ BSTR                                                         |
| PROPID- \_ ACC- \_ rolemap          | VT \_ BSTR                                                         |
| PROPID- \_ ACC- \_ statemap         | VT \_ BSTR                                                         |
| PROPID- \_ ACC- \_ Fokus            | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID- \_ ACC- \_ Auswahl        | VT \_ -Verteilung<br/> VT \_ I4<br/> VT \_ unbekannt<br/> |
| PROPID- \_ ACC über \_ geordnetes Element           | VT \_ -Verteilung                                                     |
| PROPID-ACC-Navigations- \_ \_ \_ up          | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID-ACC-Navigationsbereich \_ \_ \_        | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID- \_ ACC- \_ NAV \_ Links        | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID-ACC-Navigations \_ \_ \_ Recht       | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID- \_ ACC- \_ NAV- \_ Prev        | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID- \_ ACC- \_ NAV \_ als nächstes        | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID- \_ ACC- \_ NAV ( \_ FirstChild)  | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |
| PROPID- \_ ACC- \_ NAV- \_ LastChild   | VT \_ -Verteilung<br/> VT \_ I4<br/>                        |



 

 

