---
title: Das represent_as Attribut
description: Mit dem Attribut \represent as\ können Sie angeben, wie ein bestimmter übertragbarer Datentyp \_ für die Anwendung dargestellt wird.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Remoteprozeduraufruf RPC , Attribute, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbf217260f3d23f7390a2295d7db5a36174ae01a94f7368f8e7d2085d19ae0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923999"
---
# <a name="the-represent_as-attribute"></a>Das als \_ Attribut darstellende

Mit \[ [dem Attribut \_ "represent as"](/windows/desktop/Midl/represent-as) können Sie angeben, wie ein bestimmter übertragbarer Datentyp \] für die Anwendung dargestellt wird. Hierzu geben Sie den Namen des dargestellten Typs für einen bekannten übertragbaren Typ an und geben die Konvertierungsroutinen an. Sie müssen auch die Routinen zur Verfügung geben, um den von den Datentypobjekten verwendeten Arbeitsspeicher frei zu geben.

Verwenden Sie **\[ das -Attribut "represent \_ \] as",** um eine Anwendung mit einem anderen, möglicherweise nicht übertragbaren Datentyp anstelle des Typs zu präsentieren, der tatsächlich zwischen Client und Server übertragen wird. Es ist auch möglich, dass der Typ, den die Anwendung bearbeitet, zum Zeitpunkt der MIDL-Kompilierung unbekannt sein kann. Wenn Sie einen klar definierten übertragbaren Typ auswählen, müssen Sie sich keine Sorgen um die Datendarstellung in der heterogenen Umgebung machen. Das **\[ attribut \_ "represent as" \]** kann Ihre Anwendung effizienter gestalten, indem die Menge der über das Netzwerk übertragenen Daten reduziert wird.

Das **\[ \_ -Attribut "represent as" \]** ähnelt dem Attribut \[ ["transmit \_ as".](/windows/desktop/Midl/transmit-as) \] Bei der **\[ Übertragung \_ als \]** können Sie jedoch einen Datentyp angeben, der für die Übertragung verwendet **\[ \_ \] wird.** Mit darstellen als können Sie angeben, wie ein Datentyp für die Anwendung dargestellt wird. Der dargestellte Typ muss nicht in den midl-verarbeiteten Dateien definiert werden. sie kann zu dem Zeitpunkt definiert werden, zu dem die Stubs mit dem C-Compiler kompiliert werden. Verwenden Sie hierzu die include-Direktive in der [Anwendungskonfigurationsdatei (Application Configuration File, ACF),](the-application-configuration-file-acf-.md) um die entsprechende Headerdatei zu kompilieren. Der folgende ACF definiert z. B. einen lokalen Typ für die Anwendung, **\_ repr-Typ,** für den übersetzbaren Typ **namens \_ type:**

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

In der folgenden Tabelle werden die vier vom Programmierer bereitgestellten Routinen beschrieben.



| -Routine zurückgegebener Wert                      | BESCHREIBUNG                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **benannter \_ Typ \_ aus \_ lokalem** | Ordnet eine Instanz des Netzwerktyps zu und konvertiert vom lokalen Typ in den Netzwerktyp.      |
| **benannter \_ Typ \_ in \_ lokal**   | Konvertiert vom Netzwerktyp in den lokalen Typ.                                                    |
| **benannter \_ typ \_ free \_ local** | Gibt durch einen Aufruf des benannten Typs der lokalen Routine zugeordneten Arbeitsspeicher frei, jedoch nicht den Typ selbst. **\_ \_ \_** |
| **named \_ type \_ free \_ inst**  | Gibt Speicher für den Netzwerktyp frei (beide Seiten).                                                     |



 

Anders als bei diesen vier vom Programmierer bereitgestellten Routinen wird der benannte Typ nicht von der Anwendung bearbeitet. Der einzige für die Anwendung sichtbare Typ ist der dargestellte Typ. Die Anwendung verwendet den dargestellten Typnamen anstelle des übertragenen Typnamens in den Prototypen und Stubs, die vom Compiler generiert werden. Sie müssen den Satz von Routinen für beide Seiten festlegen.

Bei **temporären \_ benannten Typobjekten** wird der Stub den benannten freien **Typ \_ \_ \_ inst** aufrufen, um jeglichen Arbeitsspeicher frei zu geben, der durch einen Aufruf des benannten Typs aus **dem lokalen zugeordnet \_ \_ \_ wird.**

Wenn der dargestellte Typ ein Zeiger ist oder einen Zeiger enthält, muss der benannte Typ zur lokalen Routine Speicher für die Daten zuordnen, auf die die Zeiger zeigen (das dargestellte Typobjekt selbst wird vom Stub auf die übliche Weise bearbeitet). **\_ \_ \_** Für out und in werden out-Parameter eines Typs, die als oder eine seiner Komponenten darstellen, die benannte typfreie lokale Routine automatisch für die Datenobjekte aufgerufen, die das -Attribut \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in) \] enthalten. **\[ \_** **\_ \_ \_** Für **\[ in \]** -Parameter wird die **benannte \_ \_ typfreie \_** lokale Routine nur aufgerufen, wenn das **\[ -Attribut "represent \_ as" \]** auf den Parameter angewendet wurde. Wenn das Attribut auf die Komponenten des Parameters angewendet wurde, wird die freie *\* *** \_ \_ lokale**-Routine nicht aufgerufen. Die Freiungsroutinen werden für die eingebetteten Daten nicht aufgerufen, und es wird nur ein Aufruf (bezogen auf das Attribut der obersten Ebene) für einen **\[ \]** In-Only-Parameter durchgeführt.

> [!Note]  
> Es ist möglich, sowohl die Übertragung **\[ \_ \]** als als auch **\[ die Darstellung als \_ Attribute \]** auf denselben Typ anzuwenden. Beim Marshallen von Daten wird zuerst die **\[ \_ \] Darstellung** als Typkonvertierung und dann die **\[ Übertragung \_ als \]** Konvertierung angewendet. Die Reihenfolge wird umgekehrt, wenn datenverkniffen werden. Daher ordnet beim Marshalling von lokal eine Instanz eines benannten Typs zu und übersetzt sie aus einem lokalen Typobjekt in das temporäre benannte \* *_\_ \__* Typobjekt. Dieses Objekt ist das dargestellte Typobjekt, das für die \* *_\_ to \_ xmit-Routine verwendet_* wird. Die \* *_\_ zu \_ xmit-Routine_* ordnet dann ein übertragenes Typobjekt zu und übersetzt es aus dem dargestellten (benannten) Objekt in das übertragene Objekt.

 

Ein Array von langen ganzen Zahlen kann verwendet werden, um eine verknüpfte Liste zu darstellen. Auf diese Weise bearbeitet die Anwendung die Liste, und die Übertragung verwendet ein Array von langen ganzen Zahlen, wenn eine Liste dieses Typs übertragen wird. Sie können mit einem Array beginnen, aber die Verwendung eines Konstrukts mit einem offenen Array von langen ganzen Zahlen ist praktischer. Das folgende Beispiel zeigt die erforderliche Vorgehensweise.

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

Beachten Sie, dass die Prototypen der Routinen, die den **LONGARR-Typ** verwenden, tatsächlich in den Stub.h-Dateien als **PLOC \_ BOX** statt als **LONGARR-Typ angezeigt** werden. Dasselbe gilt für die entsprechenden Stubs in der \_ Stub-C.c-Datei.

Sie müssen die folgenden vier Funktionen verwenden:

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

Die oben gezeigten Routinen führen folgende Schritte aus:

-   Die **LONGARR-Routine \_ \_** aus der lokalen Routine zählt die Knoten der Liste, ordnet ein LONGARR-Objekt mit der Größe **sizeof**(**LONGARR**) + Count sizeof ( long) zu, legt das Feld Size auf Count fest und kopiert die Daten in das \* ** **DataArr-Feld.**  
-   Die **Routine LONGARR \_ to \_ local** erstellt eine Liste mit Size-Knoten und überträgt das Array an die entsprechenden Knoten.
-   Die **longarr \_ free \_ inst-Routine** gibt in diesem Fall nichts frei.
-   Die **kostenlose lokale \_ LONGARR-Routine \_** gibt alle Knoten der Liste frei.

 

 