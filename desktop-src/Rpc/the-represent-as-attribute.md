---
title: Das represent_as-Attribut
description: Mit dem Attribut \ wird \_ als \ dargestellt können Sie angeben, wie ein bestimmter, transaktionier baren Datentyp für die Anwendung dargestellt wird.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Remote Prozedur Aufruf RPC, Attribute, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102223"
---
# <a name="the-represent_as-attribute"></a>Das \_ As-Attribut.

Mithilfe des \[ Attributs [ \_ As](/windows/desktop/Midl/represent-as) \] können Sie angeben, wie ein bestimmter, transaktionier baren Datentyp für die Anwendung dargestellt wird. Dies erfolgt durch Angabe des Namens des dargestellten Typs für einen bekannten transaktionablen Typ und Bereitstellen der Konvertierungs Routinen. Sie müssen auch die Routinen bereitstellen, um den von den Datentyp Objekten genutzten Arbeitsspeicher freizugeben.

Verwenden Sie das Attribut **\[ \_ As \]** , um eine Anwendung mit einem anderen, möglicherweise nicht transaktionablen Datentyp und nicht mit dem Typ darzustellen, der tatsächlich zwischen Client und Server übertragen wird. Es ist auch möglich, dass der Typ, der von der Anwendung bearbeitet wird, zum Zeitpunkt der mittleren Kompilierung unbekannt ist. Wenn Sie einen klar definierten transaktionablen Typ auswählen, müssen Sie sich keine Gedanken über die Datendarstellung in der heterogenen Umgebung machen. Das Attribut " **\[ \_ As \]** " kann die Anwendung effizienter machen, indem die Menge der über das Netzwerk übertragenen Daten reduziert wird.

Das Attribut " **\[ \_ As \]** " ähnelt dem \[ [Übertragungs- \_ As](/windows/desktop/Midl/transmit-as) - \] Attribut. Bei der **\[ \_ \]** **\[ \_ Übertragung als können Sie jedoch einen Datentyp angeben, der für die Übertragung verwendet wird. Sie können jedoch angeben, wie ein Datentyp für die Anwendung dargestellt wird. \]** Der dargestellte Typ muss nicht in den in der Mitte verarbeiteten Dateien definiert werden. Sie kann zu dem Zeitpunkt definiert werden, zu dem die Stub mit dem C-Compiler kompiliert werden. Verwenden Sie hierzu die include-Direktive in der [Anwendungs Konfigurationsdatei (ACF)](the-application-configuration-file-acf-.md) , um die entsprechende Header Datei zu kompilieren. Die folgende ACF definiert z. b. einen lokalen Typ für die Anwendung ( **repr- \_ Typ**) für den transaktionalen Typ **namens \_ Type:**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

In der folgenden Tabelle werden die vier von Programmierern bereitgestellten Routinen beschrieben.



| -Routine zurückgegebener Wert                      | BESCHREIBUNG                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **benannter \_ Typ \_ aus \_ lokalem** | Weist eine Instanz des Netzwerk Typs zu und konvertiert vom lokalen Typ in den Netzwerktyp.      |
| **benannter \_ Typ \_ zu \_ lokal**   | Konvertiert den Netzwerktyp in den lokalen Typ.                                                    |
| **benannte \_ \_ typfreie \_ lokale** | Gibt Arbeitsspeicher frei, der durch einen-Befehl für den benannten Typ zugeordnet ist, jedoch nicht **\_ \_ für \_** den Typ selbst. |
| **benannter \_ Typ \_ ohne \_ inst**  | Gibt Speicher für den Netzwerktyp frei (beide Seiten).                                                     |



 

Der benannte Typ wird von der Anwendung nicht bearbeitet, außer von diesen vier vom Programmierer bereitgestellten Routinen. Der einzige für die Anwendung sichtbare Typ ist der dargestellte Typ. Die Anwendung verwendet den dargestellten Typnamen anstelle des übertragenen Typnamens in den Prototypen und vom Compiler generierten Stub. Sie müssen den Satz von Routinen für beide Seiten angeben.

Für temporäre **benannte \_ Typobjekte** ruft der Stub den **benannten \_ Typ " \_ Free \_ inst** " auf, um Speicher freizugeben, der durch einen aufzurufenden **\_ CallType \_ from \_ local** zugewiesen wird.

Wenn der dargestellte Typ ein Zeiger ist oder einen Zeiger enthält, muss der **benannte Typ für die \_ \_ \_ lokale** Routine Speicher für die Daten zuweisen, auf die der Zeiger verweist (das dargestellte Typobjekt selbst wird vom Stub auf die übliche Weise manipuliert). Für \[ [out](/windows/desktop/Midl/out-idl) \] -und \[ [in](/windows/desktop/Midl/in)-out- \] Parameter eines Typs, die **\[ \_ als** oder eine Komponente von darstellen, wird **die \_ benannte \_ typfreie \_ lokale** Routine automatisch für die Datenobjekte aufgerufen, die das-Attribut enthalten. Bei **\[ in \]** -Parametern wird die **benannte \_ \_ \_ lokale** Routine für den Typ nur aufgerufen, wenn das Attribut **\[ \_ As als \]** Attribut auf den Parameter angewendet wurde. Wenn das-Attribut auf die Komponenten des-Parameters angewendet wurde, wird die *\* *** \_ Kostenlose \_ local**-Routine nicht aufgerufen. Das Freigeben von Routinen wird nicht für die eingebetteten Daten und den at-most-Once-Aufruf (im Zusammenhang mit dem Attribut der obersten Ebene) **\[ \] für einen only** -Parameter aufgerufen.

> [!Note]  
> Es ist möglich, die über **\[ Tragung \_ als \]** und **\[ \_ als \]** Attribute für denselben Typ zu verwenden. Beim Marshalling von Daten wird die **\[ Darstellung \_ als \]** Typkonvertierung zuerst angewendet. Anschließend wird die über **\[ Tragung \_ als \]** Konvertierung angewendet. Die Reihenfolge wird beim Marshalling von Daten rückgängig gemacht. Folglich ordnet beim Marshalling \* **\_ von \_ local** eine Instanz eines benannten Typs zu und übersetzt Sie von einem lokalen Typobjekt in das temporäre benannte Typobjekt. Dieses Objekt ist das präsentierte Typobjekt, das für die- \* **\_ to- \_ xmit** -Routine verwendet wird. Die \* **\_ to \_ xmit** -Routine ordnet dann ein übertragener Typobjekt zu und übersetzt es vom dargestellten (benannten) Objekt in das übertragene Objekt.

 

Ein Array von Long-Integer-Werten kann verwendet werden, um eine verknüpfte Liste darzustellen. Auf diese Weise wird die Liste von der Anwendung bearbeitet, und die Übertragung verwendet ein Array von langen ganzen Zahlen, wenn eine Liste dieses Typs übertragen wird. Sie können mit einem Array beginnen, aber es ist bequemer, ein Konstrukt mit einem geöffneten Array von langen ganzen Zahlen zu verwenden. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

Beachten Sie, dass die Prototypen der Routinen, die den **longarr** -Typ verwenden, tatsächlich in den Stub. h-Dateien als **ploc- \_ Feld** anstelle des **longarr** -Typs angezeigt werden. Dasselbe gilt für die geeigneten Stubs in der Datei "Stub \_ c. c".

Sie müssen die folgenden vier Funktionen bereitstellen:

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

Die oben gezeigten Routinen gehen wie folgt vor:

-   Die **longarr \_ from \_ local** -Routine zählt die Knoten der Liste, ordnet ein longarr-Objekt mit der Größe **sizeof**(**longarr**) + count \* **sizeof**(**Long**) zu, legt das **Größen** Feld auf count fest und kopiert die Daten in das **dataarr** -Feld.
-   Die Routine **longarr \_ to \_ local** erstellt eine Liste mit Größen Knoten und überträgt das Array an die entsprechenden Knoten.
-   Die Routine " **longarr \_ Free \_ inst** " gibt in diesem Fall nichts frei.
-   Die **\_ Kostenlose \_ lokale longarr** -Routine gibt alle Knoten der Liste frei.

 

 