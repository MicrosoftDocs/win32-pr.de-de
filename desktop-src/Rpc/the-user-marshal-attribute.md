---
title: Das user_marshal-Attribut
description: Das \ User \_ Marshal \-Attribut ist ein Attribut vom Typ "ACF", das in der Syntax "\" \_ als \ darstellt.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Remote Prozedur Aufruf RPC, Attribute, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473805"
---
# <a name="the-user_marshal-attribute"></a>Das Mars-Attribut des Benutzers \_

Das \[ Attribut für den [Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal) \] ist ein Attribut vom Typ "ACF", das in der Syntax ähnlich ist \[ [ \_ als](/windows/desktop/Midl/represent-as) \] . Wie beim IDL-Attribut bietet \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] eine effizientere Möglichkeit zum Mars Hallen von Daten in einem Netzwerk. Als ACF-Attribut können Sie mithilfe von **\[ User \_ Marshal \]** benutzerdefinierte Datentypen Mars Hallen, die in der mittleren l unbekannt sind. Jeder anwendungsspezifische Typ verfügt über einen entsprechenden transaktionablen Typ, der die Wire-Darstellung definiert.

Der anwendungsspezifische Typ kann ein einfacher, zusammengesetzter oder Zeigertyp sein. Die Haupteinschränkung besteht darin, dass die Typinstanz eine festgelegte, klar definierte Speichergröße aufweisen muss. Wenn die Größe Ihrer Typinstanz geändert werden muss, verwenden Sie ein Zeiger Feld anstelle eines konformen Arrays. Alternativ können Sie einen Zeiger auf den änderbaren Typ definieren.

Wie beim Wire Marshal-Attribut stellen Sie Routinen für die Größenanpassung, das **\[ \_ Marshalling \]** , das Marshalling und das Freigeben von Durchläufen bereit. In der folgenden Tabelle werden die vier vom Benutzer bereitgestellten Routine Namen beschrieben. Der <type> ist der userm-*Typ* , der in der Typdefinition für den **\[ Benutzer- \_ Marshal \]** angegeben ist.



| -Routine zurückgegebener Wert                                                            | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Usersize](the-type-usersize-function.md)           | Gibt die Größe des RPC-Daten Puffers vor dem Mars Hallen auf Client-oder Serverseite an. |
| [<type>\_Usermarshal](the-type-usermarshal-function.md)     | Marshalls der Daten auf Client-oder Serverseite.                           |
| [<type>\_Userunmarshal](the-type-userunmarshal-function.md) | Gibt die Daten auf der Client-oder Serverseite aus.                         |
| [<type>\_Benutzer frei](the-type-userfree-function.md)           | Gibt die Daten auf der Serverseite frei.                                        |



 

Diese vom Benutzer bereitgestellten Routinen werden entweder von der Client-oder der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.

Wenn der-Parameter \[ nur [in](/windows/desktop/Midl/in) ist \] , überträgt der Client an den Server. Der Client benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ". Der Server benötigt die Funktionen **<type> \_ userunmarshal** und **<type> \_ userfree** .

Bei einem reinen \[ [out](/windows/desktop/Midl/out-idl) \] -Parameter überträgt der Server an den Client. Der Server benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ", während der Client die **<type> \_ usermarshal** -Funktion benötigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Wire \_ Marshal-Attribut](the-wire-marshal-attribute.md)
</dt> <dt>

[Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**Ndrgetusermarshalinfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 