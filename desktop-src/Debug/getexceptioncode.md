---
description: Ruft einen Code ab, der den Typ der ausgelösten Ausnahme identifiziert. Die Funktion kann nur innerhalb des Filterausdrucks oder Ausnahmehandlerblocks eines Ausnahmehandlers aufgerufen werden.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: GetExceptionCode-Makro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5c1badd5317b5a12eb97ed6418873b5c576f520f4a8106361abb1a6f7c95921e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162661"
---
# <a name="getexceptioncode-macro"></a>GetExceptionCode-Makro

Ruft einen Code ab, der den Typ der ausgelösten Ausnahme identifiziert. Die Funktion kann nur innerhalb des Filterausdrucks oder Ausnahmehandlerblocks eines Ausnahmehandlers aufgerufen werden.

> [!Note]  
> Der Microsoft C/C++-Optimierungscompiler interpretiert diese Funktion als Schlüsselwort, und seine Verwendung außerhalb der entsprechenden Ausnahmebehandlungssyntax generiert einen Compilerfehler.

 

## <a name="syntax"></a>Syntax


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert identifiziert den Typ der Ausnahme. In der folgenden Tabelle sind die Ausnahmecodes aufgeführt, die aufgrund häufiger Programmierfehler auftreten können. Diese Werte werden in WinBase.h und WinNT.h definiert.



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ AUSNAHMEZUGRIFFSVERLETZUNG**</dt> </dl>         | Der Thread versucht, aus einer virtuellen Adresse zu lesen oder in diese zu schreiben, für die er keinen Zugriff hat.<br/> Dieser Wert wird als STATUS \_ ACCESS \_ VIOLATION (STATUSZUGRIFFSVERLETZUNG) definiert.<br/>                                                                                                                                                 |
| <dl> <dt>**\_ \_ AUSNAHMEARRAY-BEGRENZUNGEN \_ ÜBERSCHRITTEN**</dt> </dl>   | Der Thread versucht, auf ein Arrayelement zu zugreifen, das sich nicht an den Grenzen befindet, und die zugrunde liegende Hardware unterstützt die Überprüfung von Begrenzungen.<br/> Dieser Wert ist als STATUS \_ ARRAY \_ BOUNDS \_ EXCEEDED definiert.<br/>                                                                                                                 |
| <dl> <dt>**EXCEPTION \_ BREAKPOINT**</dt> </dl>                | Ein Haltepunkt wird gefunden.<br/> Dieser Wert wird als STATUS \_ BREAKPOINT definiert.<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**\_AUSNAHMEDATENTYP \_ FALSCH AUSIGNMENT**</dt> </dl>    | Der Thread versucht, Daten zu lesen oder zu schreiben, die auf Hardware, die keine Ausrichtung bietet, falsch ausgerichtet sind. Beispielsweise müssen 16-Bit-Werte an 2-Byte-Grenzen ausgerichtet werden, 32-Bit-Werte an 4-Byte-Grenzen und so weiter.<br/> Dieser Wert ist als STATUS \_ DATATYPE \_ MISALIGNMENT definiert.<br/>                    |
| <dl> <dt>**EXCEPTION \_ FLT \_ DENORMAL \_ OPERAND**</dt> </dl>    | Einer der Operanden in einem Gleitkommavorgang ist denormal. Ein denormaler Wert ist ein Wert, der zu klein ist, um als Standard-Gleitkommawert zu darstellen.<br/> Dieser Wert ist als STATUS \_ FLOAT \_ DENORMAL \_ OPERAND definiert.<br/>                                                                                  |
| <dl> <dt>**EXCEPTION \_ FLT \_ DIVIDE BY \_ \_ 0**</dt> </dl>     | Der Thread versucht, einen Gleitkommawert durch einen Gleitkommateiler von 0 (null) zu dividieren.<br/> Dieser Wert ist als STATUS \_ FLOAT DIVIDE BY ZERO \_ \_ \_ definiert.<br/>                                                                                                                                               |
| <dl> <dt>**EXCEPTION \_ FLT \_ INEXACT \_ RESULT**</dt> </dl>      | Das Ergebnis einer Gleitkommaoperation kann nicht genau als Dezimalbruch dargestellt werden.<br/> Dieser Wert ist als STATUS \_ FLOAT \_ INEXACT \_ RESULT definiert.<br/>                                                                                                                                                |
| <dl> <dt>**EXCEPTION \_ FLT \_ : UNGÜLTIGER \_ VORGANG**</dt> </dl>   | Eine Gleitkommaausnahme, die nicht in dieser Liste enthalten ist.<br/> Dieser Wert ist als STATUS \_ FLOAT \_ INVALID OPERATION \_ definiert.<br/>                                                                                                                                                                             |
| <dl> <dt>**EXCEPTION \_ FLT \_ OVERFLOW**</dt> </dl>             | Der Exponent einer Gleitkommaoperation ist größer als die vom entsprechenden Typ zulässige Größe.<br/> Dieser Wert ist als STATUS \_ FLOAT \_ OVERFLOW definiert.<br/>                                                                                                                                         |
| <dl> <dt>**EXCEPTION \_ FLT \_ STACK \_ CHECK**</dt> </dl>         | Der Stapel ist aufgrund eines Gleitkomma-Vorgangs über- oder unterlaufen.<br/> Dieser Wert ist als STATUS \_ FLOAT \_ STACK CHECK \_ definiert.<br/>                                                                                                                                                                 |
| <dl> <dt>**EXCEPTION \_ FLT \_ UNDERFLOW**</dt> </dl>            | Der Exponent einer Gleitkommaoperation ist kleiner als die vom entsprechenden Typ zulässige Größe.<br/> Dieser Wert ist als STATUS \_ FLOAT \_ UNDERFLOW definiert.<br/>                                                                                                                                           |
| <dl> <dt>**EXCEPTION \_ \_ GUARD-SEITE**</dt> </dl>               | Der Thread hat auf den mit dem PAGE \_ GUARD-Modifizierer zugeordneten Arbeitsspeicher zugegriffen.<br/> Dieser Wert ist als STATUS \_ GUARD \_ PAGE VIOLATION \_ definiert.<br/>                                                                                                                                                                          |
| <dl> <dt>**AUSNAHME \_ UNGÜLTIGE \_ ANWEISUNG**</dt> </dl>      | Der Thread versucht, eine ungültige Anweisung auszuführen.<br/> Dieser Wert ist als STATUS \_ ILLEGAL \_ INSTRUCTION definiert.<br/>                                                                                                                                                                                            |
| <dl> <dt>**AUSNAHME \_ IM \_ \_ SEITENFEHLER**</dt> </dl>           | Der Thread versucht, auf eine Seite zu zugreifen, die nicht vorhanden ist, und das System kann die Seite nicht laden. Diese Ausnahme kann beispielsweise auftreten, wenn eine Netzwerkverbindung beim Ausführen eines Programms über ein Netzwerk verloren geht.<br/> Dieser Wert ist als STATUS \_ IN \_ PAGE ERROR \_ definiert.<br/>                                   |
| <dl> <dt>**EXCEPTION \_ INT \_ DIVIDE BY \_ \_ 0**</dt> </dl>     | Der Thread versucht, einen ganzzahligen Wert durch einen ganzzahligen Divisor von 0 (null) zu dividieren.<br/> Dieser Wert ist als STATUS \_ INTEGER DIVIDE BY ZERO \_ \_ \_ definiert.<br/>                                                                                                                                                         |
| <dl> <dt>**EXCEPTION \_ INT \_ OVERFLOW**</dt> </dl>             | Das Ergebnis eines ganzzahligen Vorgangs erstellt einen Wert, der zu groß ist, um vom Zielregister gehalten zu werden. In einigen Fällen führt dies dazu, dass das wichtigste Bit des Ergebnisses entsteht. Einige Vorgänge legen das Carry-Flag nicht fest.<br/> Dieser Wert ist als STATUS \_ INTEGER \_ OVERFLOW definiert.<br/> |
| <dl> <dt>**AUSNAHME \_ UNGÜLTIGE \_ DISPOSITION**</dt> </dl>      | Ein Ausnahmehandler gibt eine ungültige Disposition an den Ausnahmeverhandler zurück. Programmierer, die eine high-level-Sprache wie C verwenden, sollten nie auf diese Ausnahme stoßen.<br/> Dieser Wert ist als STATUS \_ INVALID \_ DISPOSITION definiert.<br/>                                                                      |
| <dl> <dt>**AUSNAHME \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>           | Der Thread hat ein Handle für ein ungültiges Kernelobjekt verwendet (wahrscheinlich, weil es geschlossen wurde).<br/> Dieser Wert ist als STATUS \_ INVALID \_ HANDLE definiert.<br/>                                                                                                                                                 |
| <dl> <dt>**EXCEPTION \_ NONCONTINUABLE \_ EXCEPTION**</dt> </dl> | Der Thread versucht, die Ausführung fortzufahren, nachdem eine nicht kontinuierbare Ausnahme auftritt.<br/> Dieser Wert ist als STATUS \_ NONCONTINUABLE \_ EXCEPTION definiert.<br/>                                                                                                                                                       |
| <dl> <dt>**EXCEPTION \_ \_ PRIV-ANWEISUNG**</dt> </dl>         | Der Thread versucht, eine Anweisung mit einem Vorgang auszuführen, der im aktuellen Computermodus nicht zulässig ist.<br/> Dieser Wert ist als STATUS \_ PRIVILEGED \_ INSTRUCTION definiert.<br/>                                                                                                                           |
| <dl> <dt>**EXCEPTION \_ SINGLE \_ STEP**</dt> </dl>              | Ein Ablaufverfolgungsabfang oder ein anderer einzelner Anweisungsmechanismus signalisiert, dass eine Anweisung ausgeführt wird.<br/> Dieser Wert ist als STATUS \_ SINGLE \_ STEP definiert.<br/>                                                                                                                                                           |
| <dl> <dt>**\_ \_ AUSNAHMESTAPELÜBERLAUF**</dt> </dl>           | Der Thread verwendet seinen Stapel.<br/> Dieser Wert ist als STATUS \_ STACK \_ OVERFLOW definiert.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**\_ \_ STATUSENTLADUNGSKONSOLIDIERUNG**</dt> </dl>          | Eine Framekonsolidierung wurde ausgeführt.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Hinweise

Die **GetExceptionCode-Funktion** kann nur innerhalb des Filterausdrucks oder Ausnahmehandlerblocks eines Ausnahmehandlers aufgerufen werden. Der Filterausdruck wird ausgewertet, wenn während der Ausführung des **\_ \_ try-Blocks** eine Ausnahme auftritt, und bestimmt, ob der **\_ \_ except-Block** ausgeführt wird.

Der Filterausdruck kann eine Filterfunktion aufrufen. Die Filterfunktion kann **GetExceptionCode nicht aufrufen.** Der Rückgabewert von **GetExceptionCode** kann jedoch als Parameter an eine Filterfunktion übergeben werden. Der Rückgabewert der [**GetExceptionInformation-Funktion**](getexceptioninformation.md) kann auch als Parameter an eine Filterfunktion übergeben werden. **GetExceptionInformation gibt** einen Zeiger auf eine -Struktur zurück, die die Ausnahmecodeinformationen enthält.

Wenn geschachtelte Handler vorhanden sind, wird jeder Filterausdruck ausgewertet, bis einer als EXCEPTION EXECUTE HANDLER oder \_ EXCEPTION CONTINUE EXECUTION ausgewertet \_ \_ \_ wird. Jeder Filterausdruck kann **GetExceptionCode aufrufen,** um den Ausnahmecode zu erhalten.

Der zurückgegebene Ausnahmecode ist der Von einer Hardwareausnahme generierte Code oder der code, der in der [**RaiseException-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) für eine softwaregenerierte Ausnahme angegeben ist.

Bei der Behandlung der Breakpointausnahme ist es wichtig, den Anweisungszeiger im Kontextdatensatz zu erhöhen, um von dieser Ausnahme fortzufahren.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verwenden eines Ausnahmehandlers.](using-an-exception-handler.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**Raiseexception**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Strukturierte Funktionen zur Ausnahmebehandlung](structured-exception-handling-functions.md)
</dt> <dt>

[Übersicht über die strukturierte Ausnahmebehandlung](structured-exception-handling.md)
</dt> </dl>

 

 
