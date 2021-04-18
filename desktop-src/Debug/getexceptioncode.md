---
description: Ruft einen Code ab, der den Typ der Ausnahme angibt, die auftritt. Die-Funktion kann nur innerhalb des Filter Ausdrucks oder des ausnahmehandlerblocks eines Ausnahme Handlers aufgerufen werden.
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
ms.openlocfilehash: 3b87b77ddb2d2e2af3a22e30d1204cf178ee6981
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340127"
---
# <a name="getexceptioncode-macro"></a>GetExceptionCode-Makro

Ruft einen Code ab, der den Typ der Ausnahme angibt, die auftritt. Die-Funktion kann nur innerhalb des Filter Ausdrucks oder des ausnahmehandlerblocks eines Ausnahme Handlers aufgerufen werden.

> [!Note]  
> Der Microsoft C/C++-Optimierungs Compiler interpretiert diese Funktion als Schlüsselwort, und die Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler.

 

## <a name="syntax"></a>Syntax


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert identifiziert den Typ der Ausnahme. In der folgenden Tabelle sind die Ausnahme Codes aufgeführt, die aufgrund allgemeiner Programmierfehler auftreten können. Diese Werte werden in "Winbase. h" und "Winnt. h" definiert.



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ausnahme \_ Zugriffs \_ Verletzung**</dt> </dl>         | Der Thread versucht, eine virtuelle Adresse zu lesen oder in diese zu schreiben, für die er keinen Zugriff hat.<br/> Dieser Wert wird als Status \_ Zugriffs \_ Verletzung definiert.<br/>                                                                                                                                                 |
| <dl> <dt>**Ausnahme \_ array \_ Begrenzungen \_ überschritten**</dt> </dl>   | Der Thread versucht, auf ein Array Element zuzugreifen, das außerhalb des gültigen Bereichs liegt, und die zugrunde liegende Hardware unterstützt die Überprüfung von Grenzen.<br/> Dieser Wert wird definiert, wenn die Status \_ array \_ Begrenzungen \_ überschritten wurden.<br/>                                                                                                                 |
| <dl> <dt>**Ausnahme \_ Breakpoint**</dt> </dl>                | Ein Haltepunkt ist aufgetreten.<br/> Dieser Wert wird als Status-halte \_ Punkt definiert.<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**\_Fehlausrichtung des Ausnahme Datentyps \_**</dt> </dl>    | Der Thread versucht, Daten zu lesen oder zu schreiben, die auf Hardware, die keine Ausrichtung bietet, falsch ausgerichtet sind. Beispielsweise müssen 16-Bit-Werte an 2-Byte-Begrenzungen, 32-Bit-Werten an 4-Byte-Begrenzungen usw. ausgerichtet werden.<br/> Dieser Wert wird als \_ Fehlausrichtung des Status Datentyps definiert \_ .<br/>                    |
| <dl> <dt>**Ausnahme bei der Angabe des Ausnahme- \_ \_ \_ Operanden.**</dt> </dl>    | Einer der Operanden in einer Gleit Komma Operation ist DENORMAL. Ein DENORMAL-Wert ist ein Wert, der zu klein ist, um als Standardwert für Gleit Komma Werte dargestellt zu werden.<br/> Dieser Wert wird als Status \_ float \_ -DENORMAL- \_ Operand definiert.<br/>                                                                                  |
| <dl> <dt>**Ausnahme \_ \_ bei der Trennung von "f" \_ durch \_ null**</dt> </dl>     | Der Thread versucht, einen Gleit Komma Wert durch den Gleit Komma Teiler 0 (null) zu teilen.<br/> Dieser Wert wird als Status \_ float \_ durch Null dividiert definiert \_ \_ .<br/>                                                                                                                                               |
| <dl> <dt>**\_ \_ ungenaues Ergebnis der Ausnahme \_**</dt> </dl>      | Das Ergebnis einer Gleit Komma Operation kann nicht exakt als Dezimal Bruch dargestellt werden.<br/> Dieser Wert wird als "Status \_ float \_ inexact \_ Result" definiert.<br/>                                                                                                                                                |
| <dl> <dt>**Ausnahme bei \_ \_ ungültigem f- \_ Vorgang**</dt> </dl>   | Eine Gleit Komma Ausnahme, die nicht in dieser Liste enthalten ist.<br/> Dieser Wert wird als Status \_ \_ ungültiger \_ Vorgang definiert.<br/>                                                                                                                                                                             |
| <dl> <dt>**Ausnahme- \_ f- \_ Überlauf**</dt> </dl>             | Der Exponent einer Gleit Komma Operation ist größer als die vom entsprechenden Typ zulässige Größe.<br/> Dieser Wert wird als Status Gleit \_ Komma \_ Überlauf definiert.<br/>                                                                                                                                         |
| <dl> <dt>**Ausnahme- \_ llt- \_ Stapel \_ Überprüfung**</dt> </dl>         | Der Stapel ist aufgrund eines Gleit Komma Vorgangs Überlauf oder Unterlauf.<br/> Dieser Wert wird als Status \_ float- \_ Stapel \_ Überprüfung definiert.<br/>                                                                                                                                                                 |
| <dl> <dt>**Ausnahme- \_ \_ Unterlauf**</dt> </dl>            | Der Exponent einer Gleit Komma Operation ist kleiner als die vom entsprechenden Typ zulässige Größe.<br/> Dieser Wert wird als "Status \_ float \_ underflow" definiert.<br/>                                                                                                                                           |
| <dl> <dt>**Seite "Exception \_ Guard" \_**</dt> </dl>               | Der vom Thread zugeordnete Speicher, der dem Modifizierer "page Guard" zugeordnet ist \_<br/> Dieser Wert wird als Verletzung der Status \_ Wächter \_ Seite definiert \_ .<br/>                                                                                                                                                                          |
| <dl> <dt>**Ausnahme ungültige \_ \_ Anweisung**</dt> </dl>      | Der Thread versucht, eine ungültige Anweisung auszuführen.<br/> Dieser Wert ist als ungültige \_ Status \_ Anweisung definiert.<br/>                                                                                                                                                                                            |
| <dl> <dt>**Ausnahme \_ bei \_ Seiten \_ Fehler.**</dt> </dl>           | Der Thread versucht, auf eine Seite zuzugreifen, die nicht vorhanden ist, und das System kann die Seite nicht laden. Diese Ausnahme kann beispielsweise auftreten, wenn eine Netzwerkverbindung unterbrochen wird, während ein Programm über ein Netzwerk ausgeführt wird.<br/> Dieser Wert wird als Status \_ in \_ Seiten Fehler definiert \_ .<br/>                                   |
| <dl> <dt>**Ausnahme \_ int \_ \_ durch \_ Null dividieren**</dt> </dl>     | Der Thread versucht, einen ganzzahligen Wert durch einen ganzzahligen Divisor von 0 (null) zu teilen.<br/> Dieser Wert wird als Status \_ Ganzzahl \_ dividiert \_ durch \_ null definiert.<br/>                                                                                                                                                         |
| <dl> <dt>**Exception \_ int- \_ Überlauf**</dt> </dl>             | Das Ergebnis einer ganzzahligen Operation erstellt einen Wert, der zu groß ist, um vom Ziel Register aufbewahrt zu werden. In einigen Fällen führt dies dazu, dass das Ergebnis der signifikantesten Ergebnis ist. Bei einigen Vorgängen wird das traversiflag nicht festgelegt.<br/> Dieser Wert wird als Überlauf des Status \_ Integer definiert \_ .<br/> |
| <dl> <dt>**\_ungültige \_ Disposition**</dt> </dl>      | Ein Ausnahmehandler gibt eine ungültige Disposition an den Ausnahme Verteiler zurück. Programmierer, die eine Sprache auf hoher Ebene verwenden, z. b. C, sollten diese Ausnahme nie treffen.<br/> Dieser Wert wird als Status \_ ungültige \_ Disposition definiert.<br/>                                                                      |
| <dl> <dt>**Ausnahme \_ ungültiges \_ handle**</dt> </dl>           | Der Thread hat ein Handle für ein ungültiges Kernel Objekt verwendet (wahrscheinlich, weil er geschlossen wurde).<br/> Dieser Wert ist als \_ ungültiges \_ handle definiert.<br/>                                                                                                                                                 |
| <dl> <dt>**Ausnahme \_ nicht fort Setz Bare \_ Ausnahme**</dt> </dl> | Der Thread versucht, die Ausführung fortzusetzen, nachdem eine nicht fort Setz Bare Ausnahme aufgetreten ist.<br/> Dieser Wert wird als \_ nicht fort Setz Bare Status \_ Ausnahme definiert.<br/>                                                                                                                                                       |
| <dl> <dt>**Ausnahme \_ PRIV- \_ Anweisung**</dt> </dl>         | Der Thread versucht, eine Anweisung mit einem Vorgang auszuführen, der im aktuellen Computer Modus nicht zulässig ist.<br/> Dieser Wert wird als privilegierte Status \_ \_ Anweisung definiert.<br/>                                                                                                                           |
| <dl> <dt>**Ausnahme \_ einzelner \_ Schritt**</dt> </dl>              | Ein Ablauf Verfolgungs Trap oder ein anderer Einweisungs Mechanismus signalisiert, dass eine Anweisung ausgeführt wird.<br/> Dieser Wert ist als \_ einzelner Schritt definiert \_ .<br/>                                                                                                                                                           |
| <dl> <dt>**Ausnahme \_ Stapel \_ Überlauf**</dt> </dl>           | Der Thread verwendet seinen Stapel.<br/> Dieser Wert wird als Status \_ Stapel \_ Überlauf definiert.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**Status \_ Entladung \_ konsolidieren**</dt> </dl>          | Eine Frame Konsolidierung wurde ausgeführt.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Die **GetExceptionCode** -Funktion kann nur innerhalb des Filter Ausdrucks oder des ausnahmehandlerblocks eines Ausnahme Handlers aufgerufen werden. Der Filter Ausdruck wird ausgewertet, wenn während der Ausführung des **\_ \_ try** -Blocks eine Ausnahme auftritt, und bestimmt, ob der **\_ \_ Ausnahme** Block ausgeführt wird oder nicht.

Der Filter Ausdruck kann eine Filterfunktion aufrufen. Die Filterfunktion kann " **GetExceptionCode**" nicht aufrufen. Der Rückgabewert von **GetExceptionCode** kann jedoch als Parameter an eine Filterfunktion übergeben werden. Der Rückgabewert der [**GetExceptionInformation**](getexceptioninformation.md) -Funktion kann auch als Parameter an eine Filterfunktion übergeben werden. **GetExceptionInformation** gibt einen Zeiger auf eine-Struktur zurück, die die Ausnahme Code Informationen enthält.

Wenn geschachtelte Handler vorhanden sind, wird jeder Filter Ausdruck ausgewertet, bis ein Filter Ausdruck ausgewertet wird, wenn der Ausnahme Ausführungs \_ \_ Handler oder eine Ausnahme \_ Ausführung fortgesetzt wird \_ . Jeder Filter Ausdruck kann **GetExceptionCode** aufrufen, um den Ausnahme Code zu erhalten.

Der zurückgegebene Ausnahme Code ist der Code, der durch eine Hardware Ausnahme generiert wurde, oder der Code, der in der [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) -Funktion für eine von Software generierte Ausnahme angegeben wurde.

Wenn Sie die breakpointausnahme verarbeiten, ist es wichtig, den Anweisungs Zeiger im Kontext Daten Satz zu erhöhen, um mit dieser Ausnahme fortzufahren.

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Verwenden eines Ausnahme Handlers](using-an-exception-handler.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Funktionen für die strukturierte Ausnahmebehandlung](structured-exception-handling-functions.md)
</dt> <dt>

[Übersicht über die strukturierte Ausnahmebehandlung](structured-exception-handling.md)
</dt> </dl>

 

 
