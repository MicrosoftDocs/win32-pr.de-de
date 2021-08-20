---
title: Verwenden der Serveranmerkung
description: Dieses Thema enthält Informationen zur Verwendung der Serveranmerkung zum Angeben eines Rückrufobjekts.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2955d49431b502c8587484208321bc1ab1bc0c8201fabf466b60b68f548a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823904"
---
# <a name="using-server-annotation"></a>Verwenden der Serveranmerkung

Dieses Thema enthält Informationen zur Verwendung der Serveranmerkung zum Angeben eines Rückrufobjekts.

**So überschreiben Sie eine Eigenschaft, die ein Rückrufobjekt angibt**

1.  Rufen Sie einen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) auf das barrierefreie Element ab, das mit Anmerkungen versehen werden soll.
2.  Rufen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das barrierefreie Element auf, um einen [**IAccIdentity-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) abzurufen.
3.  Rufen Sie [**IAccIdentity::GetIdentityString()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) für den [**IAccIdentity-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) auf, um eine Zeichenfolge abzurufen, die das barrierefreie Element eindeutig identifiziert, das mit Anmerkungen versehen werden soll.
4.  Verwenden Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoCreateInstanceEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) um das [**IAccPropServices-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) zu erstellen.
5.  Erstellen Sie ein Component Object Model -Objekt (COM), das [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)implementiert.
6.  Rufen Sie [**IAccPropServices::SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)auf, und übergeben Sie die Identitätszeichenfolge, eine GUID, die die zu überschreibende Eigenschaft angibt, und einen Zeiger auf das [**IAccPropServer-Rückrufobjekt.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)
7.  Gibt Schnittstellenzeiger frei und gibt Arbeitsspeicher frei.

Wenn ein Client die -Eigenschaft des barrierefreien Elements anfordert, wird das Rückrufobjekt aufgerufen und gibt den Wert an den Client zurück.

Wie bei der Angabe eines Werts können Serverentwickler alternativ die [**IAccPropServices::ComposeHwndIdentityString-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) verwenden, um eine Identitätszeichenfolge abzurufen. oder sie können die [**IAccPropServices::SetHwndPropServer-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) verwenden und die Parameter *hwnd,* *idObject* oder *idChild* anstelle einer Identitätszeichenfolge angeben.

Bei Verwendung von [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) oder [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) für ein Containerobjekt können Serverentwickler optional angeben, dass die überschreibenden Informationen auch für alle untergeordneten Elementelemente dieses Containers gelten sollen.

Server können die Anmerkung jederzeit explizit löschen, indem [**sie IAccPropServices::ClearProps verwenden.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops) Dies ist in der Regel nicht erforderlich, da der Anmerkungsdienst automatisch Anmerkungsinformationen bereinigt und freigibt, wenn das barrierefreie Element, das kommentiert wird, nicht mehr angezeigt wird.

Im Folgenden finden Sie eine Liste der Eigenschaften, die mithilfe dieser Prozedur kommentiert werden können.

## <a name="properties-supported-when-specifying-a-callback"></a>Eigenschaften, die beim Angeben eines Rückrufs unterstützt werden

Beim Angeben eines Rückrufs können die folgenden Eigenschaften mit Anmerkungen versehen werden. Derzeit können diese Eigenschaften nicht direkt durch Angabe eines Werts kommentiert werden.



| Eigenschaft                      | Typ                                                             |
|-------------------------------|------------------------------------------------------------------|
| PROPID \_ ACC \_ NAME             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DESCRIPTION      | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ROLE             | VT \_ I4                                                           |
| PROPID \_ ACC \_ STATE            | VT \_ I4                                                           |
| PROPID \_ ACC \_ HELP             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ FOCUS            | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ SELECTION        | VT \_ DISPATCH<br/> VT \_ I4<br/> VT \_ UNKNOWN<br/> |
| PROPID \_ ACC \_ PARENT           | VT \_ DISPATCH                                                     |
| PROPID \_ ACC \_ NAV \_ UP          | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ DOWN        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LEFT        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ RIGHT       | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ PREV        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ NEXT        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LASTCHILD   | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |



 

 

