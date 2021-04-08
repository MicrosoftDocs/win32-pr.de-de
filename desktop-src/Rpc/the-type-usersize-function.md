---
title: Die type_UserSize-Funktion
description: Die Type \_ usersize-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730017"
---
# <a name="the-type_usersize-function"></a>Die Type \_ usersize-Funktion

Die **<type> \_ usersize** -Funktion ist eine Hilfsfunktion für die Attribute " \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) " \] . Die Stubdateien bezeichnen diese Funktion, um die Größe des RPC-Daten Puffers für das Benutzerdaten Objekt zu verkleinern, bevor die Daten auf der Client-oder Serverseite gemarshallt werden. Die-Funktion ist wie folgt definiert:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

Der <type> im Funktionsnamen bedeutet den userm-Typ, wie in der Typdefinition für den **\[ Wire \_ \] Marshal** oder den **\[ Benutzer- \_ Marshal \]** angegeben. Dieser Typ kann nicht transaktierbar oder sogar – sein, wenn er mit dem Attribut " **\[ User \_ Marshal \]** " verwendet wird – unbekannt für den mittlerer l-Compiler. Der Name des Wire-Typs (der über das Netzwerk übertragene Typ) wird im Funktionsprototyp nicht verwendet. Beachten Sie jedoch, dass der Wire-Typ das Layout für die Daten definiert, wie von OSF DCE angegeben. Alle Daten müssen in das Format der Netzwerkdaten Darstellung (NDR) konvertiert werden.

Der *pflags* -Parameter ist ein Zeiger auf ein Feld **ohne** Vorzeichen. Das obere Wort des Flags enthält die von OSF DCE für Gleit Komma-, Byte Reihenfolge und Zeichen Darstellungen definierten NDR-Formatflags. Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert. Das genaue Layout der Flags innerhalb des Felds wird in der folgenden Tabelle gezeigt.



| Bits  | Flag                                  | Wert                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Gleit Komma Darstellung         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Ganzzahl und Gleit Komma-Byte Reihenfolge | 0 = Big-d 1 = Little----------                                                          |
| 19-16 | Zeichen Darstellung              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Marshalling von Context-Flag               | 0 = mshctx \_ Local 1 = mshctx \_ nosharedmem 2 = mshctx \_ differenentmachine 3 = mshctx \_ INPROC |



 

Das marshallingkontextflag ermöglicht es, das Verhalten der Routine abhängig vom Kontext des RPC-Aufrufs zu ändern. Wenn Sie z. b. über ein Handle (**Long**) für einen Datenblock verfügen, können Sie das Handle für einen Prozess internen-Rückruf senden, aber Sie würden die eigentlichen Daten für einen-Rückruf an einen anderen Computer senden. Das marshallingkontextflag und seine Werte werden in den Wtypes. h-und Wtypes. IDL-Dateien im Platform Software Development Kit (SDK) definiert.

> [!Note]  
> Wenn der Wire-Typ ordnungsgemäß definiert ist, müssen Sie die Format-Flags für den NDR nicht verwenden, da die NDR-Engine die erforderlichen Konvertierungen ausführt.

 

Der *startingsize* -Parameter ist der aktuelle Puffer Offset. Die Anfangs Größe gibt den Puffer Offset für das Benutzerobjekt an und kann möglicherweise nicht ordnungsgemäß ausgerichtet werden. Ihre Routine muss alle erforderlichen Auffüll Zeichen berücksichtigen.

Der *pmyobj* -Parameter ist ein Zeiger auf ein Benutzertyp Objekt.

Der Rückgabewert ist die neue Offset-oder Puffer Position. Die-Funktion sollte die kumulative Größe zurückgeben. dabei handelt es sich um die Anfangs Größe Plus mögliche Auffüll Zeichen zuzüglich der Datengröße.

Die **<type> \_ usersize** -Funktion kann eine Überschätzung der benötigten Größe zurückgeben. Die tatsächliche Größe des gesendeten Puffers wird durch die Datengröße, nicht durch die Puffer Zuordnungs Größe definiert.

Die **<type> \_ usersize** -Funktion wird nicht aufgerufen, wenn die Wire-Größe zur Kompilierzeit berechnet werden kann. Beachten Sie, dass die tatsächliche Größe der Wire-Darstellung bei den meisten Unions nur zur Laufzeit bestimmt werden kann, auch wenn keine Zeiger vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Benutzer \_ Mars Hall](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Wire \_ Marshal](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 