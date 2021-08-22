---
title: Die type_UserSize-Funktion
description: Die \_ UserSize-Funktion vom Typ ist eine Hilfsfunktion für die Attribute \wire \_ marshal\ und \user \_ marshal\.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b7c5d0918489dbc41baaa4e799aa1dbbda67723cf8104e0641ced24b9b5bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923540"
---
# <a name="the-type_usersize-function"></a>Der Typ \_ UserSize-Funktion

Die **<type> \_ UserSize-Funktion** ist eine Hilfsfunktion für die Attribute \[ ["wire \_ marshal"](/windows/desktop/Midl/wire-marshal) \] und \[ ["user \_ marshal".](/windows/desktop/Midl/user-marshal) \] Die Stubs rufen diese Funktion auf, um die Größe des RPC-Datenpuffers für das Benutzerdatenobjekt zu größe, bevor die Daten auf Client- oder Serverseite gemarshallt werden. Die Funktion ist wie die folgenden definiert:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

Der im Funktionsnamen bedeutet den userm-type, wie in der Definition des <type> **\[ Wire \_ Marshal- \]** oder **\[ \_ Benutzer-Marshalltyps \]** angegeben. Dieser Typ kann nicht übersetzt werden oder sogar – bei Verwendung mit dem **\[ \_ \] Benutzer-Marshallattribut** – für den MIDL-Compiler unbekannt sein. Der Name des Übertragungstyps (der Name des Typs, der über das Netzwerk übertragen wird) wird im Funktionsprototyp nicht verwendet. Beachten Sie jedoch, dass der Wire-Typ das Layout für die Daten definiert, wie von OSF DCE angegeben. Alle Daten müssen in das NDR-Format (Network Data Representation) konvertiert werden.

Der *pFlags-Parameter* ist ein Zeiger auf ein Feld mit langen **Flags ohne** Vorzeichen. Das obere Wort des Flags enthält NDR-Formatflags, wie von OSF DCE für Gleitkomma-, Byte- und Zeichendarstellungen definiert. Das untere Wort enthält ein Marshallingkontextflag, wie vom COM-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds ist in der folgenden Tabelle dargestellt.



| Bits  | Flag                                  | Wert                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Gleitkommadarstellung         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Ganzzahl- und Gleitkomma-Byte reihenfolge | 0 = Big-Endian 1 = Little-Endian                                                          |
| 19-16 | Zeichendarstellung              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Marshallingkontextflag               | 0 = MSHCTX \_ LOCAL 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ INPROC |



 

Das Marshallingkontextflag ermöglicht es, das Verhalten Ihrer Routine abhängig vom Kontext für den RPC-Aufruf zu ändern. Wenn Sie beispielsweise über ein Handle (**long**) für einen Datenblock verfügen, können Sie das Handle für einen Prozessaufruf senden, aber Sie würden die tatsächlichen Daten für einen Aufruf an einen anderen Computer senden. Das Marshallingkontextflag und seine Werte werden in den Dateien Wtypes.h und Wtypes.idl im Platform Software Development Kit (SDK) definiert.

> [!Note]  
> Wenn der Kabeltyp ordnungsgemäß definiert ist, müssen Sie die NDR-Formatflags nicht verwenden, da die NDR-Engine die erforderlichen Konvertierungen ausführt.

 

Der *StartingSize-Parameter* ist der aktuelle Pufferoffset. Die Anfangsgröße gibt den Pufferoffset für das Benutzerobjekt an und wird möglicherweise nicht ordnungsgemäß ausgerichtet. Ihre Routine sollte alle erforderlichen Auf padding-Daten berücksichtigen.

Der *pMyObj-Parameter* ist ein Zeiger auf ein Benutzertypobjekt.

Der Rückgabewert ist der neue Offset oder die neue Pufferposition. Die Funktion sollte die kumulative Größe zurückgeben, die die Anfangsgröße plus mögliche Auf padding plus die Datengröße ist.

Die **<type> \_ UserSize-Funktion** kann eine Überschätzung der erforderlichen Größe zurückgeben. Die tatsächliche Größe des gesendeten Puffers wird durch die Datengröße und nicht durch die Pufferzuordnungsgröße definiert.

Die **<type> \_ UserSize-Funktion** wird nicht aufgerufen, wenn die Kabelgröße zur Kompilierzeit berechnet werden kann. Beachten Sie, dass die tatsächliche Größe der Wire-Darstellung für die meisten Unions nur zur Laufzeit bestimmt werden kann, auch wenn keine Zeiger festgelegt sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshallingregeln für das \_ Marshallen von Benutzer und das Wire \_ Marshal](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_Benutzer-Marshalling](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 