---
title: Drei Zeigertypen
description: MIDL unterstützt drei Typen von Zeigern für eine Vielzahl von Anwendungen.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9627c71b07c86ab2deb7e28bddcf6d30b1747cf7d44874620f4053383a5a948a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923459"
---
# <a name="three-pointer-types"></a>Drei Zeigertypen

MIDL unterstützt drei Typen von Zeigern für eine Vielzahl von Anwendungen. Die drei verschiedenen Ebenen werden als verweis-, eindeutige und vollständige Zeiger bezeichnet und durch die Attribute **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**unique**](/windows/desktop/Midl/unique) **\]** und **\[** [**ptr**](/windows/desktop/Midl/ptr) **\]** bzw. angegeben. Die von diesen Attributen beschriebenen Zeigerklassen schließen sich gegenseitig aus. Zeigerattribute können auf Zeiger in Typdefinitionen, Funktionsrückgabetypen, Funktionsparametern, Membern von Strukturen oder Unions oder Arrayelementen angewendet werden.

Eingebettete Zeiger sind Zeiger, die Member von Strukturen oder Unions sind. Sie können auch Elemente von Arrays sein. In **\[** [**Richtung**](/windows/desktop/Midl/in) **\]** wird davon ausgegangen, dass eingebettete **\[ Verweiszeiger \]** auf gültigen Speicher zeigen und nicht NULL sein dürfen. Diese Situation gilt rekursiv für **\[ alle \] Verweiszeiger,** auf die sie verweisen. In **\[ Richtung \]** können eingebettete **\[ eindeutige \]** und vollständige Zeiger (Zeiger mit dem **\[ \] ptr-Attribut)** NULL sein oder nicht.

Jedes Zeigerattribut, das für einen Parameter in der Syntax einer Funktionsdeklaration platziert wird, wirkt sich nur auf den ganz rechten Zeigerdeklarator für diesen Parameter aus. Um andere Zeigerdeklaratoren zu beeinflussen, müssen benannte Zwischentypen verwendet werden.

Funktionen, die einen Zeiger zurückgeben, können ein Zeigerattribut als Funktionsattribut aufweisen. Die **\[ attribute unique \]** und **\[ ptr \]** müssen auf Funktionsrückgabetypen angewendet werden. Memberdeklarationen, die Zeiger sind, können ein Zeigerattribut als Feldattribut angeben. Ein Zeigerattribut kann auch als Typattribut in [**typedef-Konstrukten**](/windows/desktop/Midl/typedef) angewendet werden.

Wenn kein Zeigerattribut als Feld- oder Typattribut angegeben wird, werden Zeigerattribute gemäß den Regeln für eine nicht attributierte Zeigerdeklaration wie folgt angewendet.

Im DCE-Kompatibilitätsmodus werden Zeigerattribute in der definierenden IDL-Datei bestimmt. Wenn in der definierenden Schnittstelle ein **\[** [**\_ Zeigerstandardattribut**](/windows/desktop/Midl/pointer-default) **\]** angegeben ist, wird dieses Attribut verwendet. Wenn kein **\[ \_ \] Zeigerstandardattribut** vorhanden ist, sind alle nicht attributierten Zeiger vollständige Zeiger.

Im Microsoft-Erweiterungsmodus können Zeigerattribute durch Importieren von IDL-Dateien bestimmt werden und werden in der folgenden Reihenfolge angewendet:

1.  Ein explizites Zeigerattribut, das an der Verwendungssite angewendet wird.
2.  Das **\[ \] ref-Attribut,** wenn der nicht attributierte Zeiger ein Zeigerparameter der obersten Ebene ist.
3.  Ein in der definierenden Schnittstelle angegebenes **\[ \_ \] Zeigerstandardattribut.**
4.  Ein in der Basisschnittstelle angegebenes **\[ \_ \] Zeigerstandardattribut.**
5.  Das **\[ eindeutige \]** Attribut.

Das **\[** [**\_ Zeigerstandardschnittstellenattribut**](/windows/desktop/Midl/pointer-default) **\]** gibt die Standardzeigerattribute an, die auf einen Zeigerdeklarator in einer Typ-, Parameter- oder Rückgabetypdeklaration angewendet werden sollen, wenn auf diese Deklaration kein explizites Zeigerattribut angewendet wurde. Das **\[ \_ \] Zeigerstandardschnittstellenattribut** gilt nicht für einen nicht attributierten Zeiger der obersten Ebene eines Parameters, der als **\[ ref \]** angenommen wird.

 

 