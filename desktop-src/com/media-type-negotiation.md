---
title: Media-Type Aushandlung
description: Viele Internet Protokolle auf Anwendungsebene basieren auf dem Austausch von Nachrichten in einem einfachen, flexiblen Format namens Multipurpose Internet Mail Extensions (MIME).
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb145fa3a76da6574172ddd24888f3b5da7ad85e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391074"
---
# <a name="media-type-negotiation"></a>Media-Type Aushandlung

Viele Internet Protokolle auf Anwendungsebene basieren auf dem Austausch von Nachrichten in einem einfachen, flexiblen Format namens Multipurpose Internet Mail Extensions (MIME). Obwohl MIME als Standard für den Austausch elektronischer e-Mail-Nachrichten verwendet wird, wird Sie heute von einer Vielzahl von Anwendungen verwendet, um sich gegenseitig verständliche Datenformate als MIME-oder Media-Typen anzugeben. Der Prozess wird als *Medientyp Aushandlung* bezeichnet.

Medientypen sind einfache Zeichen folgen, die einen Typ und einen Untertyp (z. b. "Text/Plain" oder "Text/HTML") bezeichnen. Sie werden verwendet, um Daten zu bezeichnen oder eine Anforderung zu qualifizieren. Ein Webbrowser, z. b. als Teil einer HTTP-Anforderung (for-Data oder Request-for-info), gibt an, dass er die Medientypen "image/gif" oder "Image/JPEG" anfordert, auf die ein Webserver antwortet, indem er den entsprechenden Medientyp zurückgibt und, wenn es sich um eine Anforderung für Daten handelt, die Daten im angeforderten Format.

Die Medientyp-Aushandlung ähnelt oft der Aushandlung vorhandener Desktop Anwendungen mit der System Zwischenablage, um zu bestimmen, welches Datenformat eingefügt werden soll, wenn ein Benutzer beim Drag & amp; Drop einen [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Zeiger empfängt. Der feine Unterschied bei der http-Medientyp Aushandlung besteht darin, dass der Client nicht im Voraus weiß, welche Formate der Server zur Verfügung steht. Daher gibt der Client die von ihm unterstützten Medientypen in der Reihenfolge der höchsten Treue an, und der Server antwortet mit dem besten verfügbaren Format.

URL-Moniker unterstützen eine Medientyp Aushandlung als Möglichkeit für Internet Clients und-Server, um die beim Herunterladen von Daten in [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) -Vorgängen zu verwendenden Formate zu akzeptieren. Zur Unterstützung der Medientyp Aushandlung implementiert ein Client die [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) -Schnittstelle und ruft die [**registerformatenumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) -Funktion auf, um Sie beim Bindungs Kontext zu registrieren. Im Format-Enumerator werden die Formate aufgelistet, die der Client annehmen kann. Ein URL-Moniker übersetzt diese Formate bei der Bindung an HTTP-URLs in Medientypen.

Die vom Client angeforderten möglichen Medientypen werden mithilfe von [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Strukturen, die über den [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) -Enumerator verfügbar sind, der vom Aufrufer im Bindungs Kontext registriert  wird, als URL-Moniker dargestellt. Das folgende Code Fragment gibt z. b. an, dass der Medientyp PostScript ist.

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

Ein Client kann das Zwischenablage Format auf den sondermedientyp CF \_ null festlegen, um anzugeben, dass der Standard Medientyp der Ressource, auf die die URL verweist, abgerufen werden soll. Dieses Format ist in der Regel der letzte, an dem der Client interessiert ist. Wenn kein Enumerator im Bindungs Kontext registriert ist, funktioniert ein URL-Moniker so, als ob ein Enumerator, der ein einzelnes [**Formatierungs**](/windows/win32/api/objidl/ns-objidl-formatetc) Programm mit **cfFormat**= CF \_ NULL enthält, verfügbar ist, und der standardmäßige Medientyp wird automatisch heruntergeladen.

Der Medientyp, der verwendet werden soll, wird vom Client über das *pFormatetc* -Argument in der [**ibindstatuuscallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) -Methode über das pFormatetc-Argument benachrichtigt. Der Rückruf erfolgt innerhalb des Kontexts des Client Aufrufs von [**bindesstorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).

> [!Note]  
> Wenn empfangener Inhalt einen nicht erkannten Medientyp hat, ruft der Client automatisch [**registermediatypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) auf, um den neuen Typ zu registrieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[URL-Moniker](url-monikers.md)
</dt> </dl>

 

 