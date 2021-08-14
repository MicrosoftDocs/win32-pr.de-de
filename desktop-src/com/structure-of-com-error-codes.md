---
title: Struktur von COM-Fehlercodes
description: Struktur von COM-Fehlercodes
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65953582952ce076028ffcf6652e46356c4cf2afacdd088d546c2fdaafd18a33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104022"
---
# <a name="structure-of-com-error-codes"></a>Struktur von COM-Fehlercodes

Die folgende Abbildung zeigt das Format eines [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (oder SCODE). die Zahlen zeigen Bitpositionen an:

![Zeigt das Format von "H RESULT" oder "S CODE" mit Zahlen an, die Bitpositionen angeben.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

Das hochwertige Bit im **HRESULT** oder SCODE gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt. Wenn der Wert auf 0 ,SEVERITY SUCCESS" festgelegt \_ ist, gibt der Wert erfolg an. Wenn 1, SEVERITY ERROR, festgelegt \_ ist, wird ein Fehler angezeigt.

Die Bits R, C, N und r sind reserviert.

Das Feld "Facility" gibt den Systemdienst an, der für den Fehler verantwortlich ist. Microsoft ordnet neue Einrichtungscodes zu, sobald sie erforderlich werden. Die meisten SCODEs- und **HRESULT-Werte** legen das Gebäudefeld auf FACILITY \_ ITF fest, was auf einen Schnittstellenmethodenfehler hinweist.

Allgemeine Einrichtungsfelder werden in der folgenden Tabelle beschrieben.



| Feld "Facility"                | Wert        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FACILITY \_ DISPATCH<br/> | 2<br/> | Für **IDispatch-Schnittstellenfehler** mit später Bindung. <br/>                                                                                                                                                                                                                                                             |
| FACILITY \_ ITF<br/>      | 4<br/> | Für die meisten Statuscodes, die von Schnittstellenmethoden zurückgegeben werden. Die tatsächliche Bedeutung des Fehlers wird von der -Schnittstelle definiert. Das heißt, zwei **HRESULT-s** mit genau demselben 32-Bit-Wert, der von zwei verschiedenen Schnittstellen zurückgegeben wird, können unterschiedliche Bedeutungen haben. <br/>                                                       |
| FACILITY \_ NULL<br/>     | 0<br/> | Für allgemein anwendbare allgemeine Statuscodes wie Z.B. S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| FACILITY \_ RPC<br/>      | 1<br/> | Für Statuscodes, die von Remoteprozeduraufrufen zurückgegeben werden. <br/>                                                                                                                                                                                                                                                       |
| FACILITY \_ STORAGE<br/>  | 3<br/> | Für Statuscodes, die von [**IStorage-**](/windows/desktop/api/objidl/nn-objidl-istorage) oder [**IStream-Methodenaufrufen**](/windows/desktop/api/objidl/nn-objidl-istream) im Zusammenhang mit strukturiertem Speicher zurückgegeben werden. Statuscodes, deren Codewert (niedrigere 16 Bits) im Bereich der MS-DOS-Fehlercodes liegt (d.h. kleiner als 256), haben die gleiche Bedeutung wie der entsprechende MS-DOS-Fehler. <br/> |
| FACILITY \_ WIN32<br/>    | 7<br/> | Wird verwendet, um eine Möglichkeit zur Behandlung von Fehlercodes von Funktionen in der Windows-API als **HRESULT** bereitzustellen. Fehlercodes in 16-Bit-OLE, die doppelte Systemfehlercodes enthalten, wurden ebenfalls in FACILITY \_ WIN32 geändert. <br/>                                                                                                 |
| FACILITY \_ WINDOWS<br/>  | 8<br/> | Wird für zusätzliche Fehlercodes von von Microsoft definierten Schnittstellen verwendet.<br/>                                                                                                                                                                                                                                            |



 

Das Codefeld ist eine eindeutige Zahl, die zugewiesen wird, um den Fehler oder die Warnung darzustellen.

Gemäß der Konvention weisen **HRESULT-Werte** in der Regel Namen im folgenden Format auf: *Facility* \_ *Severity* \_ *Reason*.

*Die Einrichtung* ist entweder der Name der Einrichtung oder ein anderer Unterscheidungsbezeichner. *Der Schweregrad* ist ein einzelner Buchstabe, S oder E, der angibt, ob der Funktionsaufruf erfolgreich war (S) oder einen Fehler erzeugt hat (E); und *Reason* ist ein Bezeichner, der die Bedeutung des Codes beschreibt. Der Statuscode STG \_ E \_ FILENOTFOUND gibt beispielsweise an, dass ein speicherbezogener Fehler aufgetreten ist. Insbesondere ist keine angeforderte Datei vorhanden. Statuscodes aus FACILITY \_ NULL enthalten das *Facility-Präfix* \_ nicht.

Fehlercodes werden im Kontext einer Schnittstellenimplementierungen definiert. Nach der Definition können Erfolgscodes nicht mehr geändert oder neue Erfolgscodes hinzugefügt werden. Es können jedoch neue Fehlercodes geschrieben werden. Microsoft behält sich das Recht vor, neue Fehlercodes (aber keine Erfolgscodes) für die in FACILITY ITF oder in neuen Einrichtungen beschriebenen Schnittstellen zu \_ definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in COM](error-handling-in-com.md)
</dt> <dt>

[Windows Protokolle: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

