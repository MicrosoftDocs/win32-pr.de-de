---
title: Das size_is-Attribut
description: Das \ size \_ is \-Attribut ist einer ganzzahligen Konstante, einem Ausdruck oder einer Variablen zugeordnet, die die Zuordnungs Größe des Arrays angibt.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858308"
---
# <a name="the-size_is-attribute"></a>Die \[ Größe \_ ist " \] Attribute".

Die \[ [Größe \_ ist](/windows/desktop/Midl/size-is) " \] Attribute" ist einer ganzzahligen Konstante, einem Ausdruck oder einer Variablen zugeordnet, die die Zuordnungs Größe des Arrays angibt. Stellen Sie sich ein Zeichen Array vor, dessen Länge durch Benutzereingaben bestimmt wird:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> Das Sternchen ( \* ), das den Platzhalter für die Variable Array Dimension markiert, ist optional.

 

Der Serverstub muss Arbeitsspeicher auf dem Server zuweisen, der dem Arbeitsspeicher auf dem Client für diesen Parameter entspricht. Die Variable, die die Größe angibt, muss immer mindestens ein \[ [in](/windows/desktop/Midl/in) - \] Parameter sein. Das **\[ in \]** direktionale Attribut ist erforderlich, damit der Size-Wert beim Eintrag für den Serverstub definiert wird. Dieser Größen Wert enthält Informationen, die der Serverstub benötigt, um den Arbeitsspeicher zuzuordnen.

Der Size-Parameter kann sich auch \[ in, [out](/windows/desktop/Midl/out-idl)befinden \] . Dies ist beispielsweise hilfreich, wenn das vom Client gesendete Array für die Daten, die der Server speichern muss, nicht groß genug ist. Sie können einen **\[ in-, out \]** -size-Parameter verwenden, um die erforderliche Größe zurück an das Client Programm zu senden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mehrere Ebenen von Zeigern](multiple-levels-of-pointers.md)
</dt> </dl>

 

 