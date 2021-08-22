---
title: IDL-Techniken für einen besseren Schnittstellen- und Methodenentwurf
description: Erwägen Sie die Verwendung der folgenden IDL-spezifischen Techniken, um die Sicherheit und Leistung zu verbessern, wenn Sie RPC-Schnittstellen und -Methoden entwickeln, die sowohl konforme als auch varianten Daten verarbeiten.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3608e908742d4de4b6564787c6d8faffc29efcef81549ff50414cc7716c468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929426"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>IDL-Techniken für einen besseren Schnittstellen- und Methodenentwurf

Erwägen Sie die Verwendung der folgenden IDL-spezifischen Techniken, um die Sicherheit und Leistung zu verbessern, wenn Sie RPC-Schnittstellen und -Methoden entwickeln, die sowohl konforme als auch varianten Daten verarbeiten. Die attribute, auf die in diesem Thema verwiesen wird, sind die IDL-Attribute, die für Methodenparameter festgelegt sind, die entweder konforme Daten (z. B. \[ **die Größe \_ ist** \] und max \[ **\_ Attribute)** oder \] Variant-Daten (z. B. \[ **länge \_ ist** \] und \[ **Zeichenfolgenattribute)** \] verarbeiten.

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Verwenden des \[ \] Bereichsattributs mit konformen Datenparametern

Das \[  \] Bereichsattribut weist die RPC-Laufzeit an, während des Prozesses zum Aufheben der Datenmarshaling eine zusätzliche Größenüberprüfung durchzuführen. Insbesondere wird überprüft, ob die angegebene Größe der als zugeordneter Parameter übergebenen Daten innerhalb des angegebenen Bereichs liegt.

Das \[  \] Bereichsattribut wirkt sich nicht auf das Kabelformat aus.

Wenn der Wert für die Leitung außerhalb des zulässigen Bereichs liegt, löst RPC eine RPC \_ X \_ INVALID \_ BOUND- oder RPC X BAD \_ \_ \_ STUB \_ DATA-Ausnahme aus. Dies bietet eine zusätzliche Ebene der Datenvalidierung und kann dazu beitragen, häufige Sicherheitsfehler wie Pufferüberläufe zu vermeiden. Ebenso kann die Verwendung von \[ **Range** \] die Anwendungsleistung verbessern, da konforme Daten, die mit ihr gekennzeichnet sind, klar definierte Einschränkungen zur Verfügung stehen, die vom RPC-Dienst berücksichtigt werden können.

## <a name="rpc-server-stub-memory-management-rules"></a>RPC Server Stub Memory Management Rules

Beim Erstellen der IDL-Dateien für eine RPC-fähige Anwendung ist es wichtig, die Verwaltungsregeln für den RPC-Serverstubspeicher zu verstehen. Anwendungen können die Serverressourcennutzung verbessern, indem \[ **sie den Bereich** in Verbindung mit \] konformen Daten verwenden, wie oben beschrieben, und absichtlich die Anwendung von IDL-Attributen variabler Länge vermeiden, z. B. \[ **length \_ auf** \] konforme Daten.

Die Anwendung der \[ **Länge \_ wird** \] auf Datenstrukturfelder, die in einer IDL-Datei definiert sind, nicht empfohlen.

## <a name="best-practices-for-variable-length-data-parameters"></a>Bewährte Methoden für Datenparameter variabler Länge

Im Folgenden werden mehrere bewährte Methoden beschrieben, die beim Definieren der IDL-Attribute für Datenstrukturen variabler Größe, Methodenparameter und Felder zu berücksichtigen sind.

-   Verwenden Sie eine frühe Korrelation. Im Allgemeinen ist es besser, den Variablengrößenparameter oder das Feld so zu definieren, dass er unmittelbar nach dem steuernden integralen Typ auftritt.

    Beispiel:

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    besser als

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    dabei deklariert **earlyCorr** den Size-Parameter unmittelbar vor dem Datenparameter variabler Länge und **lateCorr** den size-Parameter danach. Durch die frühzeitige Entsprechung wird die Leistung insgesamt verbessert, insbesondere in Fällen, in denen die Methode häufig aufgerufen wird.

-   Bei Parametern, die mit dem Out markiert \[ **sind, \_ ist size** ein \] Attributtupel, und wenn die Datenlänge auf clientseitiger Seite bekannt ist oder wenn der Client eine angemessene Obergrenze aufweist, sollte die Methodendefinition in Bezug auf Parameterzuordnung und Sequenz etwa wie folgt lauten:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    In diesem Fall stellt der Client einen Puffer mit fester Größe für *pArr* bereit, sodass der serverseitige RPC-Dienst einen Puffer mit angemessener Größe mit einem guten Maß an Sicherheit zuordnen kann. Beachten Sie, dass im Beispiel die Daten vom Server empfangen werden ( \[ **out** \] ). Die Definition ist für Daten ähnlich, die an den Server übergeben werden ( \[ **in** \] ).

-   In Situationen, in denen die serverseitige Komponente einer RPC-Anwendung die Datenlänge bestimmt, sollte die Methodendefinition in etwa wie folgt lauten:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **RANGED \_ LONG** ist ein Typ, der sowohl für den Client- als auch für den Serverstub definiert ist, und mit einer angegebenen Größe, die der Client ordnungsgemäß antizipieren kann. Im Beispiel übergibt der Client *ppArr* als **NULL,** und die RPC-Serveranwendungskomponente ordnet die richtige Menge an Arbeitsspeicher zu. Nach der Rückgabe belegt der RPC-Dienst auf clientseitiger Seite den Arbeitsspeicher für die zurückgegebenen Daten.

-   Wenn der Client eine Teilmenge eines großen konformen Arrays an den Server senden möchte, kann die Anwendung die Größe der Teilmenge angeben, wie im folgenden Beispiel gezeigt:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    Auf diese Weise überträgt RPC nur *lLength-Elemente* des Arrays über das Kabel. Diese Definition erzwingt jedoch, dass der RPC-Dienst Speicher der Größe *lSize* auf serverseitiger Seite zuweist.

-   Wenn die Clientanwendungskomponente die maximale Größe eines Arrays bestimmt, das der Server zurückgeben kann, aber dem Server ermöglicht, eine Teilmenge dieses Arrays zu übertragen, kann die Anwendung ein solches Verhalten angeben, indem sie die IDL ähnlich dem folgenden Beispiel definiert:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    Die Clientanwendungskomponente gibt die maximale Größe des Arrays an, und der Server gibt an, wie viele Elemente an den Client übertragen werden.

-   Wenn die Serveranwendungskomponente eine Zeichenfolge an die Clientanwendungskomponente zurückgeben muss und der Client die maximale Größe kennt, die vom Server zurückgegeben werden soll, kann die Anwendung einen konformen Zeichenfolgentyp verwenden, wie im folgenden Beispiel gezeigt:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Wenn die Clientanwendungskomponente die Größe der Zeichenfolge nicht steuern soll, kann der RPC-Dienst den Arbeitsspeicher wie im folgenden Beispiel gezeigt explizit zuordnen:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    Die Clientanwendungskomponente muss *ppStr* beim Aufrufen der RPC-Methode auf **NULL** festlegen.

 

 




