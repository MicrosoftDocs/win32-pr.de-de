---
title: Das user_marshal Attribut
description: Das \user marshal\-Attribut ist ein ACF-Typattribut, das in der Syntax \_ mit \represent \_ as\ vergleichbar ist.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Remoteprozeduraufruf RPC , Attribute, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769e6a7e176d5aeba68afd322cdd6f24d76c6b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883748"
---
# <a name="the-user_marshal-attribute"></a>Das \_ Marshallattribut des Benutzers

Das \[ [ \_ Benutzer-Marshallattribut](/windows/desktop/Midl/user-marshal) \] ist ein ACF-Typattribut, das in der Syntax ähnlich wie \[ [ \_ ist.](/windows/desktop/Midl/represent-as) \] Wie beim IDL-Attribut, \[ [wire \_ marshal,](/windows/desktop/Midl/wire-marshal)bietet es eine effizientere Möglichkeit zum Marshallen von Daten \] über ein Netzwerk. Als ACF-Attribut können Sie **\[ mit dem \_ Benutzer-Marshalling \]** benutzerdefinierte Datentypen marshallen, die für MIDL unbekannt sind. Jeder anwendungsspezifische Typ verfügt über einen entsprechenden übertragbaren Typ, der die Übertragungsdarstellung definiert.

Ihr anwendungsspezifischer Typ kann ein einfacher, zusammengesetzter oder Zeigertyp sein. Die Haupteinschränkung ist, dass die Typinstanz eine feste, klar definierte Arbeitsspeichergröße haben muss. Wenn sich die Größe Ihrer Typinstanz ändern muss, verwenden Sie ein Zeigerfeld anstelle eines konformen Arrays. Alternativ können Sie einen Zeiger auf den änderungsbaren Typ definieren.

Wie beim **\[ Wire \_ Marshal-Attribut \]** geben Sie Routinen für die Größen-, Marshalling-, Unmarshaling- und Freeing-Läufe an. In der folgenden Tabelle werden die vier vom Benutzer bereitgestellten Routinenamen beschrieben. Der &lt; Typ ist der &gt; userm-Typ,*der* in der Definition des **\[ \_ Benutzer-Marshalltyps \]** angegeben ist.



| -Routine zurückgegebener Wert                                                            | Beschreibung                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [&lt;Geben Sie &gt; \_ UserSize ein.](the-type-usersize-function.md)           | Größe des RPC-Datenpuffers vor dem Marshalling auf Client- oder Serverseite. |
| [&lt;geben &gt; \_ Sie UserMarshal ein.](the-type-usermarshal-function.md)     | Marshallt die Daten auf Client- oder Serverseite.                           |
| [&lt;geben &gt; \_ Sie UserUnmarshal ein.](the-type-userunmarshal-function.md) | Entmarshalt die Daten auf client- oder serverseitiger Seite.                         |
| [&lt;type &gt; \_ UserFree](the-type-userfree-function.md)           | Gibt die Daten auf serverseitiger Seite frei.                                        |



 

Diese vom Benutzer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.

Wenn sich der Parameter \[ [nur in](/windows/desktop/Midl/in) \] befindet, überträgt der Client an den Server. Der Client benötigt die **&lt; Funktionen &gt; \_ UserSize** und **&lt; &gt; \_ UserMarshal.** Der Server benötigt den **&lt; Typ &gt; \_ UserUnmarshal und** die **&lt; &gt; \_ UserFree-Funktionen.**

Bei einem \[ [](/windows/desktop/Midl/out-idl) \] out-only-Parameter überträgt der Server an den Client. Der Server benötigt die **&lt; Funktionen &gt; \_ UserSize** und **&lt; &gt; \_ UserMarshal,** während der Client den Typ **&lt; &gt; \_ UserMarshal-Funktion** benötigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Wire \_ Marshal-Attribut](the-wire-marshal-attribute.md)
</dt> <dt>

[Marshallingregeln für das Marshallen von Benutzer und das Marshallen von \_ Wire](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_Benutzer-Marshalling](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 
