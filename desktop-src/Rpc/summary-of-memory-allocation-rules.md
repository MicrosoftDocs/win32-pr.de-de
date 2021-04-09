---
title: Zusammenfassung der Speicher Belegungs Regeln
description: In der folgenden Tabelle werden die wichtigsten Regeln bezüglich der Speicher Belegung zusammengefasst.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102007"
---
# <a name="summary-of-memory-allocation-rules"></a>Zusammenfassung der Speicher Belegungs Regeln

In der folgenden Tabelle werden die wichtigsten Regeln bezüglich der Speicher Belegung zusammengefasst.



| Mittel l-Element                                                                                                                                           | BESCHREIBUNG                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verweis Zeiger der \[ [obersten Ebene](/windows/desktop/Midl/ref) \]                                                                                                                | Muss Zeiger sein, die nicht NULL sind.                                                                                                                                            |
| Funktionsrückgabewert                                                                                                                                  | Neuer Arbeitsspeicher wird immer für Zeiger Rückgabewerte zugeordnet.                                                                                                             |
| \[[Unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] oder \[ [ptr](/windows/desktop/Midl/ptr), out- \] Zeiger                                                                   | Von der mittleren l nicht zugelassen.                                                                                                                                                  |
| \[ [Eindeutige](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in)-, [out](/windows/desktop/Midl/out-idl) -oder PTR-Werte der obersten Ebene, \] die sich \[ [](/windows/desktop/Midl/ptr) \] von NULL in nicht-NULL ändern | Clientstubspeicher weisen bei der Rückgabe neuen Arbeitsspeicher auf dem Client zu.                                                                                                                 |
| Eindeutiger eindeutiger \[ , [in](/windows/desktop/Midl/in)-, [out](/windows/desktop/Midl/out-idl) -Zeiger, der von einem [](/windows/desktop/Midl/unique) \] nicht-NULL-Wert in NULL geändert wird.                                 | Der Arbeitsspeicher ist auf dem Client verwaist. die Client Anwendung ist dafür verantwortlich, Arbeitsspeicher freizugeben und Verluste zu verhindern.                                                              |
| \[ [Ptr](/windows/desktop/Midl/ptr) [in](/windows/desktop/Midl/in)der obersten Ebene, in, [out](/windows/desktop/Midl/out-idl) -Zeiger, der sich \] von einem nicht-NULL-Wert in NULL ändert                                       | Der Arbeitsspeicher wird auf dem Client verwaist, wenn kein Alias vorhanden ist. die Client Anwendung ist in diesem Fall für das Freigeben und verhindern von Speicher Verlusten verantwortlich.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Zeiger                                                                                                                           | Client-Anwendungsebene wird in der Regel zugeordnet.                                                                                                                           |
| Nicht-NULL \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) - \] Zeiger                                                                                                | Stub versucht, auf dem Client in den vorhandenen Speicher zu schreiben. Wenn die **\[ Zeichenfolge \]** und die Größe die Größe überschreiten, die auf dem Client zugewiesen ist, führt dies bei der Rückgabe zu einem GP-Fehler. |



 

In der folgenden Tabelle werden die Auswirkungen der wichtigsten IDL-und ACF-Attribute auf die Speicherverwaltung zusammengefasst.



| Mittel l-Funktion                                                                   | Clientprobleme                                                                                                                                  | Serverprobleme                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[zuordnen](/windows/desktop/Midl/allocate)(einzelner \_ Knoten) \] , \[ zuordnen (alle \_ Knoten)\]         | Bestimmt, ob ein oder mehrere Aufrufe an die Speicherfunktionen vorgenommen werden.                                                                         | Identisch mit dem Client, mit Ausnahme des privaten Speichers, der häufig zum zuordnen (einzelner \_ Knoten) \[ in \] und \[ in, out- \] Daten verwendet werden kann.               |
| \[zuordnen (Free) \] oder \[ zuordnen (nicht \_ frei)\]                                 | (Keine, wirkt sich auf den Server aus.)                                                                                                                        | Bestimmt, ob der Arbeitsspeicher auf dem Server nach jedem Remote Prozedur aufzurufen freigegeben wird.                                            |
| maximale Anzahl von Array Attributen \[ [ \_ ](/windows/desktop/Midl/max-is) \] und \[ [Größe \_ ](/windows/desktop/Midl/size-is)\] | (Keine, wirkt sich auf den Server aus.)                                                                                                                        | Bestimmt die Größe des Arbeitsspeichers, der zugewiesen werden soll.                                                                                    |
| \[[Byte \_ Anzahl](/windows/desktop/Midl/byte-count)\]                                            | Der Client muss Puffer zuordnen. nicht zugeordnet oder durch clientstubspeicher freigegeben.                                                                           | Das ACF-Parameter Attribut bestimmt die Größe des auf dem Server zugewiesenen Puffers.                                                        |
| \[[ \_ zuordnen aktivieren](/windows/desktop/Midl/enable-allocate)\]                                  | Normalerweise keine. Der Client verwendet jedoch möglicherweise eine andere Speicher Verwaltungs Umgebung.                                                     | Der Server verwendet eine andere Speicher Verwaltungs Umgebung. [**Rpcsmallob**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) sollte für Zuordnungen verwendet werden. |
| \[[in](/windows/desktop/Midl/in) \] versehen                                                    | Client Anwendung, die für die Zuweisung von Speicher für Daten verantwortlich ist.                                                                                 | Wird auf dem Server durch stubspeicher zugewiesen.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] versehen                                             | Auf dem Client durch stubspeicher zugewiesen.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] -der einzige Zeiger muss ein \[ [ref](/windows/desktop/Midl/ref) - \] Zeiger sein; wird auf dem Server durch stufs zugewiesen.                       |
| \[[ref](/windows/desktop/Midl/ref) \] versehen                                                 | Der durch Zeiger referenzierte Speicher muss von der Client Anwendung zugewiesen werden.                                                                          | Verweis Zeiger der obersten Ebene und der ersten Ebene, die von stubden verwaltet werden.                                                                |
| \[[eindeutig](/windows/desktop/Midl/unique) \] versehen                                           | Ein nicht-NULL-Wert auf NULL kann zu verwaisten Arbeitsspeicher führen. NULL für nicht-NULL bewirkt, dass der Client-Stub die Benutzer Zuordnungen in der [Mitte \_ \_ ](/windows/desktop/Midl/midl-user-allocate-1)aufruft. | (Wirkt sich auf Client aus.)                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] versehen                                                 | (Siehe \[ [eindeutig](/windows/desktop/Midl/unique) \] .)                                                                                                              | (Siehe \[ [eindeutig](/windows/desktop/Midl/unique) \] .)                                                                                             |



 

 

 