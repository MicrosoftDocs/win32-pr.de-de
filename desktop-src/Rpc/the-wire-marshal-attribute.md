---
title: Das Wire_marshal-Attribut
description: Das Attribut \ Wire \_ Marshal \ ist ein Attribut vom Typ IDL, das der Syntax in \ Übertragung \_ als \ ähnelt, bietet jedoch eine effizientere Möglichkeit zum Mars Hallen von Daten über ein Netzwerk.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- Remote Prozedur Aufruf RPC, Attribute, Wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390712"
---
# <a name="the-wire_marshal-attribute"></a>Das Wire \_ Marshal-Attribut

Das \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] -Attribut ist ein Attribut vom Typ IDL, das in der Syntax für die über \[ [Tragung \_ als](/windows/desktop/Midl/transmit-as)ähnlich ist \] , aber eine effizientere Möglichkeit zum Mars Hallen von Daten in einem Netzwerk bietet.

Sie verwenden das \[ **Wire \_ Marshal** - \] Attribut, um einen Datentyp anzugeben, der anstelle des anwendungsspezifischen Datentyps übertragen wird. Jeder anwendungsspezifische Typ verfügt über einen entsprechenden transaktionablen Typ, der die Wire-Darstellung definiert (die im Netzwerk verwendete Darstellung). Der anwendungsspezifische Typ muss nicht transaktierbar sein, aber es muss sich um einen Typ handeln, der von der Mittell erkannt wird. Verwenden Sie zum Mars Hallen eines Typs, der in der mittleren l unbekannt ist, das ACF-Attribut \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] .

Der anwendungsspezifische Typ kann ein einfacher, zusammengesetzter oder Zeigertyp sein. Die Haupteinschränkung besteht darin, dass die Typinstanz eine festgelegte, klar definierte Speichergröße aufweisen muss. Wenn die Größe Ihrer Typinstanz geändert werden muss, verwenden Sie ein Zeiger Feld anstelle eines konformen Arrays. Alternativ können Sie einen Zeiger auf den änderbaren Typ definieren.

Sie müssen die Routinen für die Größenanpassung, das Marshalling und das Marshalling der Daten sowie das Freigeben des zugeordneten Speichers bereitstellen. In der folgenden Tabelle werden die vier vom Benutzer bereitgestellten Routine Namen beschrieben. Der <type> ist der in der \[ Typdefinition des **Wire \_ Marshal** angegebene userm-Typ \] .



| -Routine zurückgegebener Wert                                                            | BESCHREIBUNG                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Usersize](the-type-usersize-function.md)           | Gibt die Größe des RPC-Daten Puffers vor dem Mars Hallen auf Client-oder Serverseite an. |
| [<type>\_Usermarshal](the-type-usermarshal-function.md)     | Marshalls der Daten auf Client-oder Serverseite.                           |
| [<type>\_Userunmarshal](the-type-userunmarshal-function.md) | Gibt die Daten auf der Client-oder Serverseite aus.                         |
| [<type>\_Benutzer frei](the-type-userfree-function.md)           | Gibt die Daten auf der Serverseite frei.                                        |



 

Diese vom Programmierer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.

Wenn der-Parameter \[ nur [in](/windows/desktop/Midl/in) ist \] , überträgt der Client an den Server. Der Client benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ". Der Server benötigt die **<type> \_ userunmarshal**-und **<type> \_ userfree** -Funktionen.

Bei einem reinen \[ [out](/windows/desktop/Midl/out-idl) \] -Parameter überträgt der Server an den Client. Der Server benötigt die Funktionen " **<type> \_ usersize** " und " **<type> \_ usermarshal** ", während der Client die **<type> \_ usermarshal** -Funktion benötigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Mars-Attribut des Benutzers \_](the-user-marshal-attribute.md)
</dt> <dt>

[Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**Ndrgetusermarshalinfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 