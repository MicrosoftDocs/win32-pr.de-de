---
title: Zusammenfassung der Speicherzuordnungsregeln
description: In der folgenden Tabelle sind die wichtigsten Regeln für die Speicherzuweisung zusammengefasst.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec50632693ad0df7ff44aa1d2a9a2760b07a2ed1b72a13ac5dc33294569c3484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924701"
---
# <a name="summary-of-memory-allocation-rules"></a>Zusammenfassung der Speicherzuordnungsregeln

In der folgenden Tabelle sind die wichtigsten Regeln für die Speicherzuweisung zusammengefasst.



| MIDL-Element                                                                                                                                           | BESCHREIBUNG                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ [Ref-Zeiger der obersten](/windows/desktop/Midl/ref) \] Ebene                                                                                                                | Muss Nicht-NULL-Zeiger sein.                                                                                                                                            |
| Rückgabewert der Funktion                                                                                                                                  | Für Zeiger-Rückgabewerte wird immer neuer Arbeitsspeicher zugeordnet.                                                                                                             |
| \[[unique,](/windows/desktop/Midl/unique) [out](/windows/desktop/Midl/out-idl) \] oder \[ [ptr,](/windows/desktop/Midl/ptr) \] out-Zeiger                                                                   | Von MIDL nicht zulässig.                                                                                                                                                  |
| Eindeutiger Zeiger auf nicht oberster Ebene in , out oder \[ [](/windows/desktop/Midl/unique) [](/windows/desktop/Midl/in) [](/windows/desktop/Midl/out-idl) \] \[ [ptr](/windows/desktop/Midl/ptr)in , out-Zeiger, der von NULL in \] Nicht-NULL geändert wird | Clientstubs weisen bei der Rückgabe neuen Arbeitsspeicher auf dem Client zu.                                                                                                                 |
| Eindeutiger Zeiger auf nicht \[ [oberster Ebene](/windows/desktop/Midl/unique) [in](/windows/desktop/Midl/in), [der](/windows/desktop/Midl/out-idl) von Null in \] NULL geändert wird                                 | Der Arbeitsspeicher ist auf dem Client verwaist. Die Clientanwendung ist dafür verantwortlich, Arbeitsspeicher frei zu geben und Lecks zu verhindern.                                                              |
| Nicht-Ptr der obersten Ebene \[ [](/windows/desktop/Midl/ptr) [in](/windows/desktop/Midl/in), out-Zeiger, der sich von [](/windows/desktop/Midl/out-idl) \] Nicht-NULL in NULL ändert                                       | Der Arbeitsspeicher ist auf dem Client verwaist, wenn kein Alias verwendet wird. Die Clientanwendung ist in diesem Fall für die Freistellung und Verhinderung von Speicherverlusten verantwortlich.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Zeiger                                                                                                                           | Die Clientanwendungsebene wird in der Regel zuteilen.                                                                                                                           |
| Nicht NULL \[ [in](/windows/desktop/Midl/in), [](/windows/desktop/Midl/out-idl) \] Out-Zeiger                                                                                                | Stubs versuchen, in vorhandenen Speicher auf dem Client zu schreiben. Wenn **\[ Zeichenfolge \]** und Größe größer als die auf dem Client zugeordnete Größe sind, verursacht dies bei der Rückgabe einen GP-Fehler. |



 

In der folgenden Tabelle werden die Auswirkungen der wichtigsten IDL- und ACF-Attribute auf die Speicherverwaltung zusammengefasst.



| MIDL-Feature                                                                   | Clientprobleme                                                                                                                                  | Serverprobleme                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[allocate](/windows/desktop/Midl/allocate) \_ (einzelner Knoten), \] \[ allocate(alle \_ Knoten)\]         | Bestimmt, ob mindestens ein Aufruf der Speicherfunktionen erfolgt.                                                                         | Identisch mit dem Client, mit der Ausnahme, dass privater Arbeitsspeicher häufig für die Zuordnung (einzelner Knoten) in und \_ \[ \] \[ in,out-Daten verwendet werden \] kann.               |
| \[allocate(free) \] oder \[ allocate(don't \_ free)\]                                 | (Keine; wirkt sich auf den Server aus.)                                                                                                                        | Bestimmt, ob nach jedem Remoteprozeduraufruf Arbeitsspeicher auf dem Server frei wird.                                            |
| array attributes \[ [max is \_ and](/windows/desktop/Midl/max-is) \] size \[ [ \_ is](/windows/desktop/Midl/size-is)\] | (Keine; wirkt sich auf den Server aus.)                                                                                                                        | Bestimmt die Größe des zu reservierten Arbeitsspeichers.                                                                                    |
| \[[ \_ Byteanzahl](/windows/desktop/Midl/byte-count)\]                                            | Der Client muss den Puffer zuordnen. wird nicht von Clientstubs zugeordnet oder frei.                                                                           | Das ACF-Parameterattribut bestimmt die Größe des auf dem Server zugeordneten Puffers.                                                        |
| \[[ \_ "Allocate" aktivieren](/windows/desktop/Midl/enable-allocate)\]                                  | In der Regel keine. Der Client verwendet jedoch möglicherweise eine andere Speicherverwaltungsumgebung.                                                     | Der Server verwendet eine andere Speicherverwaltungsumgebung. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) sollte für Zuordnungen verwendet werden. |
| \[[in](/windows/desktop/Midl/in) \] Attribut                                                    | Clientanwendung, die für die Zuweisung von Arbeitsspeicher für Daten verantwortlich ist.                                                                                 | Wird auf dem Server durch Stubs zugeordnet.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] Attribut                                             | Wird auf dem Client durch Stubs zugeordnet.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] Der Zeiger "-only" muss \[ [ein](/windows/desktop/Midl/ref) \] Verweiszeiger sein, der auf dem Server durch Stubs zugeordnet wird.                       |
| \[[ref](/windows/desktop/Midl/ref) \] Attribut                                                 | Arbeitsspeicher, auf den vom Zeiger verwiesen wird, muss von der Clientanwendung zugeordnet werden.                                                                          | Verweiszeiger auf oberster und erster Ebene, die von Stubs verwaltet werden.                                                                |
| \[[unique](/windows/desktop/Midl/unique) \] Attribut                                           | Nicht NULL bis NULL kann zu verwaisten Arbeitsspeicher führen. Null bis Nicht-NULL bewirkt, dass der Clientstub [midl \_ aufruft, der dem Benutzer \_ zugibt.](/windows/desktop/Midl/midl-user-allocate-1) | (Wirkt sich auf den Client aus.)                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] Attribut                                                 | (Siehe \[ [eindeutig](/windows/desktop/Midl/unique) \] .)                                                                                                              | (Siehe \[ [eindeutig](/windows/desktop/Midl/unique) \] .)                                                                                             |



 

 

 