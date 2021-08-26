---
title: Das transmit_as Attribut
description: The \ transmit\_as\ attribute offers a way to control data marshaling without worrying about marshaling data at a low level \ 8212;that is, without worrying about data sizes or byte swapping in a heterogeneous environment.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Remoteprozeduraufruf RPC , Attribute, transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617422c50bae46de72bac1e548b6f248b19d0cb2436ac0c08b265bbba4f5a6cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016640"
---
# <a name="the-transmit_as-attribute"></a>Die Übertragung \_ als Attribut

The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment. Indem Sie die Menge der über das Netzwerk übertragenen Daten reduzieren können, kann die **\[ Übertragung \_ \]** als Attribut Ihre Anwendung effizienter gestalten.

Sie verwenden das **\[ Attribut transmit \_ as \]** , um einen Datentyp anzugeben, den die RPC-Stubs über das Netzwerk übertragen, anstatt den von der Anwendung bereitgestellten Datentyp zu verwenden. Sie geben Routinen an, die den Datentyp in den und aus dem Typ konvertieren, der für die Übertragung verwendet wird. Sie müssen auch Routinen zur Verfügung geben, um den für den Datentyp und den übertragenen Typ verwendeten Arbeitsspeicher frei zu geben. Im folgenden Beispiel wird der **\_ xmit-Typ** als der Datentyp definiert, der für alle Anwendungsdaten übertragen wird, die als typtypspezifikation **angegeben \_ sind:**

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

In der folgenden Tabelle werden die vier vom Programmierer bereitgestellten Routinenamen beschrieben. **Type** ist der Datentyp, der der Anwendung bekannt ist, und **der \_ xmit-Typ** ist der für die Übertragung verwendete Datentyp.



| -Routine zurückgegebener Wert                                                 | Beschreibung                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**type \_ to \_ xmit**](the-type-to-xmit-function.md)     | Ordnet ein Objekt des übertragenen Typs zu und konvertiert vom Anwendungstyp in den Typ, der über das Netzwerk übertragen wird (Aufrufer und Objekt aufgerufen). |
| [**Typ \_ aus \_ xmit**](the-type-from-xmit-function.md) | Konvertiert vom übertragenen Typ in den Anwendungstyp (Aufrufer und Aufgerufenes Objekt).                                                                  |
| [**Geben Sie \_ free \_ inst ein.**](the-type-free-inst-function.md) | Gibt ressourcen frei, die vom Anwendungstyp verwendet werden (objekt nur aufgerufen).                                                                              |
| [**Geben Sie \_ free \_ xmit ein.**](the-type-free-xmit-function.md) | Gibt vom Typ zurückgegebenen Speicher **für** _\__ *_die \_ xmit-Routine_* frei (Aufrufer und Objekt aufgerufen).                                                      |



 

Anders als bei diesen vier vom Programmierer bereitgestellten Funktionen wird der übertragene Typ nicht von der Anwendung bearbeitet. Der übertragene Typ wird nur definiert, um Daten über das Netzwerk zu verschieben. Nachdem die Daten in den von der Anwendung verwendeten Typ konvertiert wurden, wird der vom übertragenen Typ verwendete Arbeitsspeicher frei.

Diese vom Programmierer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt. Wenn sich der Parameter **\[** [**nur in**](/windows/desktop/Midl/in) **\]** befindet, überträgt der Client an den Server. Der Client benötigt den **Typ , \_ um \_ xmit zu verwenden** und kostenlose **\_ \_ xmit-Funktionen ein** geben zu können. Der Server benötigt den **Typ \_ von \_ xmit** und **typ free \_ \_ inst** Functions. Bei einem **\[** [](/windows/desktop/Midl/out-idl) **\]** out-only-Parameter überträgt der Server an den Client. Die Serveranwendung muss den -Typ implementieren, um **\_ \_ xmit-** und **\_ \_ free-Xmit-Funktionen** zu verwenden, während das Clientprogramm den Typ der **\_ \_ xmit-Funktion zur Verfügung** stellen muss. Für die  **temporären xmit-Typobjekte \_** wird der Stub vom Typ free xmit aufrufen, um jeglichen Arbeitsspeicher frei zu geben, der durch einen Aufruf des Typs _\__ *_\__* **von \_ \_ xmit zugeordnet wird.**

Bestimmte Richtlinien gelten für die Anwendungstypinstanz. Wenn der Anwendungstyp ein Zeiger ist oder einen Zeiger enthält, muss der Typ der \_ **\_ xmit-Routine** Speicher für die Daten zuordnen, auf die die Zeiger zeigen (das Anwendungstypobjekt selbst wird vom Stub auf die übliche Weise bearbeitet).

Für **\[ out- \]** **\[ und \] \]** out-Parameter oder eine ihrer Komponenten eines Typs, der die Übertragung als Attribut enthält, wird der typfreie **\[ \_ \]** \_ **\_ inst-Routine** automatisch für die Datenobjekte aufgerufen, die über das -Attribut verfügen. Für **in** -Parameter wird die  \_ **typfreie \_ inst-Routine** nur aufgerufen, wenn **\[ das Attribut transmit \_ as \]** auf den Parameter angewendet wurde. Wenn das -Attribut auf die Komponenten des -Parameters angewendet wurde, wird **der** Typ \_ **free \_ inst** routine nicht aufgerufen. Es gibt keine Freirufe für die eingebetteten Daten und mindestens einen Aufruf (im Zusammenhang mit dem Attribut der obersten Ebene) für einen **in** only-Parameter.

Ab MIDL 2.0 müssen Client und Server alle vier Funktionen erfüllen. Beispielsweise kann eine verknüpfte Liste als Array mit Größe übertragen werden. Der **Zu \_ \_ xmit-Typ** durchfing die verknüpfte Liste und kopiert die geordneten Daten in ein Array. Die Arrayelemente sind so geordnet, dass die vielen Zeiger, die der Listenstruktur zugeordnet sind, nicht übertragen werden müssen. Der **Typ aus der \_ \_ xmit-Routine** liest das Array und legt seine Elemente in eine Struktur mit verknüpften Listen ab.

Die doppelverknüpfungsbasierte Liste (DOUBLE LINK LIST) enthält Daten und Zeiger \_ \_ auf die vorherigen und nächsten Listenelemente:

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

Anstatt die komplexe Struktur zu versenden, kann **\[** [**das Attribut "transmit \_ as"**](/windows/desktop/Midl/transmit-as) verwendet werden, um es als Array über **\]** das Netzwerk zu senden. Die Reihenfolge der Elemente im Array behält die Reihenfolge der Elemente in der Liste zu geringeren Kosten bei:

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

Das **\[ Attribut transmit \_ as \]** wird in der IDL-Datei angezeigt:

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

Im folgenden Beispiel definiert **ModifyListProc** den Parameter vom Typ DOUBLE \_ LINK TYPE als \_ **\[ in-, \] out-Parameter:**

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

Die vier vom Programmierer definierten Funktionen verwenden den Namen des Typs in den Funktionsnamen und die dargestellten und übertragenen Typen nach Bedarf als Parametertypen:

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

 

 