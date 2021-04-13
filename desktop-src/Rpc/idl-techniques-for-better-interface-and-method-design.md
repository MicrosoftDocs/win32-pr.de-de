---
title: IDL-Techniken für einen besseren Schnittstellen-und Methoden Entwurf
description: Verwenden Sie die folgenden IDL-spezifischen Techniken, um die Sicherheit und Leistung bei der Entwicklung von RPC-Schnittstellen und-Methoden zu verbessern, die sowohl konforme als auch Variant-Daten verarbeiten.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388228"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a>IDL-Techniken für einen besseren Schnittstellen-und Methoden Entwurf

Verwenden Sie die folgenden IDL-spezifischen Techniken, um die Sicherheit und Leistung bei der Entwicklung von RPC-Schnittstellen und-Methoden zu verbessern, die sowohl konforme als auch Variant-Daten verarbeiten. Die Attribute, auf die in diesem Thema verwiesen wird, sind die IDL-Attribute, die für Methoden Parameter festgelegt werden, die entweder konforme Daten verarbeiten (z. b. die \[ **\_ Größe** \] und die \[ **Maximale \_** \] Anzahl von Attributen) oder Variant-Daten (z. b. die \[ **Länge \_** \] und \[ **Zeichen** folgen \] Attribute).

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a>Verwenden des \[ Range- \] Attributs mit kompatiblen Daten Parametern

Das \[ **Range** \] -Attribut weist die RPC-Laufzeit an, während des Daten unmarshallingprozesses eine zusätzliche Größenüberprüfung auszuführen. Insbesondere wird überprüft, ob die angegebene Größe der Daten, die als zugeordneter Parameter übergeben werden, innerhalb des angegebenen Bereichs liegt.

Das \[ **Range** - \] Attribut wirkt sich nicht auf das Wire-Format aus.

Wenn der Wert für Wire außerhalb des zulässigen Bereichs liegt, löst RPC eine \_ ungültige RPC x \_ - \_ gebundene oder RPC x-Daten Ausnahme für einen ungültigen \_ \_ \_ Stub aus \_ . Dadurch wird eine zusätzliche Ebene der Datenüberprüfung ermöglicht, und häufige Sicherheitsfehler wie Pufferüberläufe können vermieden werden. Ebenso \[  \] kann durch die Verwendung von Range die Anwendungsleistung verbessert werden, da konforme Daten, die mit diesem gekennzeichnet sind, klar definierte Einschränkungen für den RPC-Dienst zur Verfügung stehen.

## <a name="rpc-server-stub-memory-management-rules"></a>Regeln für die Speicherverwaltung von RPC-Server-Stubs

Beim Erstellen der IDL-Dateien für eine RPC-fähige Anwendung ist es wichtig, dass Sie die Regeln für die Verwaltung von RPC-Server-Stubs verstehen. Anwendungen können die Auslastung der Server Ressourcen verbessern, indem Sie einen \[ **Bereich** \] in Verbindung mit konformen Daten wie oben angegeben verwenden, und die Anwendung von Daten-IDL-Attributen variabler Länge wie etwa \[ **length \_** \] in Übereinstimmung mit Daten vermeiden.

Die Anwendung der \[ **Länge \_ erfolgt** \] auf Datenstruktur Felder, die in einer IDL-Datei definiert sind, wird nicht empfohlen.

## <a name="best-practices-for-variable-length-data-parameters"></a>Bewährte Methoden für Daten Parameter mit variabler Länge

Nachfolgend sind einige bewährte Methoden zu beachten, die beim Definieren der IDL-Attribute für Datenstrukturen variabler Größen, Methoden Parameter und Felder zu beachten sind.

-   Frühe Korrelation verwenden. Es ist in der Regel besser, den Variablen Größen Parameter oder das Feld so zu definieren, dass er unmittelbar nach dem steuernden ganzzahligen Typ auftritt.

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

    Dabei deklariert **earlycorr** den size-Parameter direkt vor dem Daten Parameter mit variabler Länge, und **latecorr** deklariert den size-Parameter danach. Mithilfe der frühen Korrespondenz wird die Leistung insgesamt verbessert, insbesondere in Fällen, in denen die-Methode häufig aufgerufen wird.

-   Bei Parametern, die mit "out" gekennzeichnet sind \[ **, \_ ist "size** " ein \] Attribut-Tupel, und wenn die Daten Länge auf der Clientseite bekannt ist oder der Client über eine vernünftige obere Grenze verfügt, sollte die Methoden Definition der folgenden in Bezug auf die Parameter Zuordnung und-Reihenfolge ähneln:

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    In diesem Fall stellt der Client einen Puffer mit fester Größe für die *Bir* bereit, sodass der serverseitige RPC-Dienst einen Puffer mit hoher Sicherheit zuordnen kann. Beachten Sie, dass im Beispiel die Daten vom Server ( \[ **out** \] ) empfangen werden. Die Definition ist für Daten, die an den Server übermittelt werden, ähnlich ( \[ **in** \] ).

-   In Situationen, in denen die serverseitige Komponente einer RPC-Anwendung die Daten Länge bestimmt, sollte die Methoden Definition wie folgt aussehen:

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    **Bereichs \_ Long** ist ein Typ, der sowohl für den Client-als auch für den serverstubwert und für eine angegebene Größe definiert ist. Im Beispiel übergibt der Client *pparr* als **null**, und die RPC-Server Anwendungs Komponente ordnet die richtige Arbeitsspeicher Menge zu. Bei der Rückgabe ordnet der RPC-Dienst auf der Clientseite den Arbeitsspeicher für die zurückgegebenen Daten zu.

-   Wenn der Client eine Teilmenge eines großen konformen Arrays an den Server senden möchte, kann die Anwendung die Größe der Teilmenge angeben, wie im folgenden Beispiel gezeigt:

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    Auf diese Weise überträgt RPC nur *llength* -Elemente des Arrays über das Netzwerk. Diese Definition zwingt jedoch den RPC-Dienst, Arbeitsspeicher der Größe *LSIZE* auf der Serverseite zuzuweisen.

-   Wenn die Client Anwendungs Komponente die maximale Größe eines Arrays bestimmt, das vom Server zurückgegeben werden kann, aber der Server die Übertragung einer Teilmenge dieses Arrays ermöglicht, kann die Anwendung ein solches Verhalten angeben, indem die IDL ähnlich dem folgenden Beispiel definiert wird:

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    Die Client Anwendungs Komponente gibt die maximale Größe des Arrays an, und der Server gibt an, wie viele Elemente zurück an den Client übermittelt werden.

-   Wenn die Server Anwendungs Komponente eine Zeichenfolge an die Client Anwendungs Komponente zurückgeben muss und der Client die maximale Größe kennt, die vom Server zurückgegeben werden soll, kann die Anwendung wie im folgenden Beispiel gezeigt einen konformen Zeichen Folgentyp verwenden:

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   Wenn die Client Anwendungs Komponente die Größe der Zeichenfolge nicht steuern soll, kann der RPC-Dienst den Arbeitsspeicher explizit zuordnen, wie im folgenden Beispiel gezeigt:

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    Beim Aufrufen der RPC-Methode muss bei der Client Anwendungs Komponente *ppstr* auf **null** festgelegt werden.

 

 




