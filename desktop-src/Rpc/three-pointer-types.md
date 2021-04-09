---
title: Drei Zeiger Typen
description: Die Mittel l unterstützt drei Arten von Zeigern für eine Vielzahl von Anwendungen.
ms.assetid: 6684c252-6fbe-49ca-9967-6d4baf5dc298
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdcc9548568c8fca24d8abb40bf0eaa8b6e7da3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948784"
---
# <a name="three-pointer-types"></a>Drei Zeiger Typen

Die Mittel l unterstützt drei Arten von Zeigern für eine Vielzahl von Anwendungen. Die drei verschiedenen Ebenen werden als Verweis-, eindeutige und vollständige Zeiger bezeichnet und werden durch die Attribute **\[** [**ref**](/windows/desktop/Midl/ref) **\]** , **\[** [**Unique**](/windows/desktop/Midl/unique)und **\]** **\[** [**ptr**](/windows/desktop/Midl/ptr)angegeben **\]** . Die von diesen Attributen beschriebenen Zeiger Klassen schließen sich gegenseitig aus. Zeiger Attribute können auf Zeiger in Typdefinitionen, Funktions Rückgabe Typen, Funktionsparametern, Member von Strukturen oder Unions oder Array Elementen angewendet werden.

Eingebettete Zeiger sind Zeiger, die Member von Strukturen oder Unions sind. Sie können auch Elemente von Arrays sein. In der **\[** [](/windows/desktop/Midl/in) **\]** Richtung wird **\[ \]** angenommen, dass eingebettete Verweis Zeiger auf einen gültigen Speicher verweisen und dürfen nicht NULL sein. Diese Situation ist rekursiv **\[ \] auf alle Verweis** Zeiger anwendbar, auf die Sie verweisen. In Richtung ( **\[ in \]** Richtung) können eingebettete **\[ eindeutige \]** und vollständige Zeiger (Zeiger mit dem **\[ ptr \]** -Attribut) oder nicht NULL sein.

Alle Zeiger Attribute, die für einen Parameter in der Syntax einer Funktionsdeklaration platziert werden, wirken sich nur auf den äußersten rechten Zeiger Deklarator für diesen Parameter aus. Um andere Zeiger Deklaratoren zu beeinflussen, müssen zwischen benannte Typen verwendet werden.

Funktionen, die einen Zeiger zurückgeben, können über ein Zeiger Attribut als Funktions Attribut verfügen. Die Attribute **\[ Unique \]** und **\[ ptr \]** müssen auf Funktions Rückgabe Typen angewendet werden. Member-Deklarationen, die Zeiger sind, können ein Zeiger Attribut als Feld Attribut angeben. Ein Zeiger Attribut kann auch als Type-Attribut in [**typedef**](/windows/desktop/Midl/typedef) -Konstrukten angewendet werden.

Wenn kein Zeiger Attribut als Feld-oder Typattribut angegeben wird, werden Zeiger Attribute entsprechend den Regeln für eine nicht attributierte Zeiger Deklaration wie folgt angewendet.

Im DCE-Kompatibilitätsmodus werden Zeiger Attribute in der definierenden IDL-Datei bestimmt. Wenn **\[** [**\_**](/windows/desktop/Midl/pointer-default) **\]** in der definierenden Schnittstelle ein Zeiger-Standard Attribut angegeben ist, wird dieses Attribut verwendet. Wenn kein **\[ Zeiger \_ - \] Standard** Attribut vorhanden ist, sind alle nicht attributierten Zeiger vollständige Zeiger.

Im Microsoft-Erweiterungs Modus können Zeiger Attribute durch Importieren von IDL-Dateien bestimmt werden und werden in der folgenden Reihenfolge angewendet:

1.  Ein explizites Zeiger Attribut, das auf der Website verwendet wird.
2.  Das **\[ ref \]** -Attribut, wenn der nicht attributierte Zeiger ein Zeiger Parameter der obersten Ebene ist.
3.  Ein **\[ Zeiger \_ Standard \]** Attribut, das in der definierenden Schnittstelle angegeben ist.
4.  Ein **\[ Zeiger \_ Standard \]** Attribut, das in der Basisschnittstelle angegeben wird.
5.  Das **\[ eindeutige \]** Attribut.

Das **\[** [**\_ standardmäßige Zeiger**](/windows/desktop/Midl/pointer-default) **\]** Schnittstellen Attribut gibt die Standard Zeiger Attribute an, die auf einen zeigerdeklarator in einer Typ-, Parameter-oder Rückgabetyp Deklaration angewendet werden sollen, wenn auf diese Deklaration kein explizites Zeiger Attribut angewendet wird. Das **\[ \_ Standard \] mäßige Zeiger** -Schnittstellen Attribut gilt nicht für einen nicht attributierten Zeiger auf oberster Ebene eines Parameters, der als **\[ ref \]** angenommen wird.

 

 