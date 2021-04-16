---
title: Das Transmit_as-Attribut
description: Das Attribut "\ \_ übertragen als \" bietet eine Möglichkeit, das Datenmarshalling zu steuern, ohne sich Gedanken über das Marshalling von Daten auf niedriger Ebene \ 8212 zu machen, d. h. ohne sich Gedanken über Datengrößen oder Byte Austausch Vorgänge in einer heterogenen Umgebung zu machen.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Remote Prozedur Aufruf RPC, Attribute, Transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390713"
---
# <a name="the-transmit_as-attribute"></a>Das Attribut "übertragen \_ als"

Das **\[** Attribut "über [**tragen \_ als**](/windows/desktop/Midl/transmit-as) " **\]** bietet eine Möglichkeit, das Marshalling von Daten zu steuern, ohne sich Gedanken über das Marshalling von Daten auf niedriger Ebene zu machen, d. –., ohne sich Gedanken über Datengrößen oder Byte Austausch Vorgänge in einer heterogenen Umgebung Wenn Sie die Menge der über das Netzwerk übertragenen Daten reduzieren können, kann das Attribut "über **\[ tragen \_ als \]** " Ihre Anwendung effizienter gestalten.

Verwenden Sie das Attribut "über **\[ tragen \_ als \]** ", um einen Datentyp anzugeben, der von den RPC-Stubdaten über das Netzwerk übertragen wird, anstatt den von der Anwendung bereitgestellten Datentyp zu verwenden. Sie stellen Routinen bereit, die den Datentyp in und aus dem Typ konvertieren, der für die Übertragung verwendet wird. Sie müssen auch Routinen bereitstellen, um den für den Datentyp und den übertragenen Typ verwendeten Arbeitsspeicher freizugeben. Im folgenden Beispiel wird der **xmit- \_ Typ** als Datentyp definiert, der für alle Anwendungsdaten übertragen wird, die als Typ der **\_ Typspezifikation** angegeben sind:

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

In der folgenden Tabelle werden die vier von Programmierern bereitgestellten Routine Namen beschrieben. **Type** ist der Datentyp, der der Anwendung bekannt ist, und der **\_ Typ xmit** ist der Datentyp, der für die Übertragung verwendet wird.



| -Routine zurückgegebener Wert                                                 | BESCHREIBUNG                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_in \_ xmit eingeben**](the-type-to-xmit-function.md)     | Ordnet ein Objekt des übertragenen Typs zu und konvertiert vom Anwendungstyp in den Typ, der über das Netzwerk (Aufrufer und Objekt aufgerufen) übertragen wird. |
| [**Typ \_ von \_ xmit**](the-type-from-xmit-function.md) | Konvertiert einen übertragenen Typ in einen Anwendungstyp (Aufrufer und Objekt mit dem Namen).                                                                  |
| [**Geben Sie " \_ Free \_ inst**](the-type-free-inst-function.md) | Gibt Ressourcen frei, die vom Anwendungstyp verwendet werden (nur Objekt aufgerufen).                                                                              |
| [**Geben Sie "Free" ein. \_ \_**](the-type-free-xmit-function.md) | Gibt den vom Typ zurückgegebenen Speicher *****\_*** für die \_ xmit** -Routine frei (Aufrufer und Objekt aufgerufen).                                                      |



 

Mit Ausnahme dieser vier vom Programmierer bereitgestellten Funktionen wird der übertragene Typ nicht von der Anwendung bearbeitet. Der übertragene Typ wird nur zum Verschieben von Daten über das Netzwerk definiert. Nachdem die Daten in den von der Anwendung verwendeten Typ konvertiert wurden, wird der vom übertragenen Typ verwendete Arbeitsspeicher freigegeben.

Diese vom Programmierer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt. Wenn der-Parameter **\[** nur [**in**](/windows/desktop/Midl/in) ist **\]** , überträgt der Client an den Server. Der Client benötigt den **Typ \_ , um \_ xmit** -und- **\_ typfreie \_ xmit** -Funktionen zu geben. Der Server benötigt den **Typ \_ von \_ xmit** und **die \_ typfreien \_ inst** -Funktionen. Bei einem reinen **\[** [**out**](/windows/desktop/Midl/out-idl) **\]** -Parameter überträgt der Server an den Client. Die Serveranwendung muss den **Typ \_ in \_ xmit** und den **Typ " \_ freie \_ xmit** -Funktionen" implementieren, während das Client Programm den **Typ aus der \_ \_ xmit** -Funktion bereitstellen muss. Bei den temporären **xmit- \_ Typobjekten** ruft der Stub den **Typ " ***\_*** Free \_ xmit** " auf, um Speicher freizugeben, der durch einen aufrufungstyp **\_ zu \_ xmit** belegt wird.

Bestimmte Richtlinien gelten für die Anwendungstyp Instanz. Wenn der Anwendungstyp ein Zeiger ist oder einen Zeiger enthält, muss der **Typ** \_ **aus der \_ xmit** -Routine Speicher für die Daten zuweisen, auf die die Zeiger zeigen (das Anwendungstyp Objekt selbst wird vom Stub auf die übliche Weise manipuliert).

Für **\[ out \]** -und **\[ in-, out- \] out \]** -Parameter oder eine der zugehörigen Komponenten eines Typs, der das Attribut "über **\[ tragen \_ als \]** " enthält, wird die **Type** \_ **Free \_ inst** -Routine automatisch für die Datenobjekte aufgerufen, die über das-Attribut verfügen. Bei **in** -Parametern wird die  \_ **typfreie \_ inst** -Routine nur aufgerufen, wenn das über **\[ tragen \_ als \]** -Attribut auf den Parameter angewendet wurde. Wenn das-Attribut auf die Komponenten des-Parameters angewendet wurde,  \_ wird die **typfreie \_ inst** -Routine nicht aufgerufen. Es gibt keine Freigabe Aufrufe für die eingebetteten Daten und höchstens einen Aufruf (im Zusammenhang mit dem Attribut der obersten Ebene) **für einen nur** -Parameter.

Mit der mittleren l 2,0 müssen sowohl der Client als auch der Server alle vier Funktionen bereitstellen. Beispielsweise kann eine verknüpfte Liste als Array mit Größenanpassung übertragen werden. Der **Typ \_ für die \_ xmit** -Routine durchläuft die verknüpfte Liste und kopiert die geordneten Daten in ein Array. Die Array Elemente sind so angeordnet, dass die vielen Zeiger, die der Listenstruktur zugeordnet sind, nicht übertragen werden müssen. Der **Typ \_ aus der \_ xmit** -Routine liest das Array und fügt seine Elemente in eine verknüpfte Listenstruktur ein.

Die Liste mit doppelten Verknüpfungen (Double \_ Link \_ List) enthält Daten und Zeiger auf die vorherigen und nächsten Listenelemente:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

Anstatt die komplexe Struktur **\[** zu versenden, kann das [**Übertragungs- \_ As**](/windows/desktop/Midl/transmit-as) - **\]** Attribut verwendet werden, um es über das Netzwerk als Array zu senden. Die Reihenfolge der Elemente in der Liste wird durch die Reihenfolge der Elemente im Array zu geringeren Kosten beibehalten:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

Das Attribut "über **\[ tragen \_ als \]** " wird in der IDL-Datei angezeigt:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

Im folgenden Beispiel definiert **modifylistproc** den Parameter vom Typ Double- \_ \_ Linktyp als in- **\[ , \] out** -Parameter:

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

Die vier vom Programmierer definierten Funktionen verwenden den Namen des Typs in den Funktionsnamen und verwenden die dargestellten und übertragenen Typen wie erforderlich als Parametertypen:

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 