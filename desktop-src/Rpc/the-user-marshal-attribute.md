---
title: Das user_marshal-Attribut
description: Das \_ \user marshal\-Attribut ist ein ACF-Typattribut, das in der Syntax ähnlich ist wie \represent \_ as\.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Remoteprozeduraufruf RPC , Attribute, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0501cfd3199d41a49da7f54919c86f9332ce976f33963f23c63a7938338da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923530"
---
# <a name="the-user_marshal-attribute"></a>Das \_ Marshallingattribut des Benutzers

Das \[ [ \_ Marshallingattribut](/windows/desktop/Midl/user-marshal) des Benutzers \] ist ein ACF-Typattribut, das in der Syntax ähnlich ist und als dargestellt \[ [ \_ wird.](/windows/desktop/Midl/represent-as) \] Wie beim IDL-Attribut , \[ [Wire \_ Marshal,](/windows/desktop/Midl/wire-marshal) \] bietet es eine effizientere Möglichkeit, Daten über ein Netzwerk zu marshallen. Als ACF-Attribut können Sie mit **\[ dem \_ Benutzer-Marshalling \]** benutzerdefinierte Datentypen marshallen, die MIDL unbekannt sind. Jeder anwendungsspezifische Typ verfügt über einen entsprechenden übertragungsfähigen Typ, der die Wire-Darstellung definiert.

Ihr anwendungsspezifischer Typ kann ein einfacher, zusammengesetzter oder Zeigertyp sein. Die Haupteinschränkung besteht darin, dass die Typinstanz über eine feste, klar definierte Arbeitsspeichergröße verfügen muss. Wenn sich die Größe Ihrer Typinstanz ändern muss, verwenden Sie ein Zeigerfeld anstelle eines konformen Arrays. Alternativ können Sie einen Zeiger auf den veränderlichen Typ definieren.

Wie beim **\[ Wire \_ \] Marshal-Attribut** stellen Sie Routinen für größen-, marshalling-, unmarshaling- und freeing-Läufe zur Verfügung. In der folgenden Tabelle werden die vier benutzerdefinierten Routinenamen beschrieben. ist <type> der benutzerbasierte *Typ,* der in der Definition des **\[ \_ \] Marshallingtyps** des Benutzers angegeben ist.



| -Routine zurückgegebener Wert                                                            | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | Größen des RPC-Datenpuffers vor dem Marshalling auf Client- oder Serverseite. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Marshallt die Daten auf Client- oder Serverseite.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Entmarshals der Daten auf Client- oder Serverseite.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Gibt die Daten auf serverseitiger Seite frei.                                        |



 

Diese vom Benutzer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.

Wenn sich der Parameter nur \[ [in](/windows/desktop/Midl/in) \] befindet, überträgt der Client an den Server. Der Client benötigt die Funktionen **<type> \_ UserSize** und **<type> \_ UserMarshal.** Der Server benötigt die Funktionen **<type> \_ UserUnmarshal** und **<type> \_ UserFree.**

Bei einem \[ [](/windows/desktop/Midl/out-idl) \] out-only-Parameter überträgt der Server an den Client. Der Server benötigt die Funktionen **<type> \_ UserSize** und **<type> \_ UserMarshal,** während der Client die **<type> \_ UserMarshal-Funktion** benötigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Wire \_ Marshal-Attribut](the-wire-marshal-attribute.md)
</dt> <dt>

[Marshallingregeln für Das Marshalling von Benutzern und das Wire \_ Marshal](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_Benutzer-Marshalling](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 