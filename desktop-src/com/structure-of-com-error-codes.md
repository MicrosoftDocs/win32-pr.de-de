---
title: Struktur von com-Fehler Codes
description: Struktur von com-Fehler Codes
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb27143f50028592f6fe0aeb5cab9795dcd10d4a
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104561773"
---
# <a name="structure-of-com-error-codes"></a>Struktur von com-Fehler Codes

Die folgende Abbildung zeigt das Format eines [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (oder SCODE). die Zahlen geben Bitpositionen an:

![Zeigt das Format von "H-Ergebnis" oder "Code" mit Zahlen an, die Bitpositionen angeben.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

Das höchst wertige Bit in **HRESULT** oder SCODE gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt. Wenn der Wert auf 0 festgelegt ist, \_ gibt der Wert Erfolg an. Wenn der Wert auf 1 festgelegt ist, \_ weist dies auf einen Fehler hin.

Die Bits r, C, N und r sind reserviert.

Das Feld "Einrichtung" gibt den Systemdienst an, der für den Fehler verantwortlich ist. Microsoft ordnet neue Einrichtungs Codes zu, sobald Sie benötigt werden. Die meisten scodes und **HRESULT** -Werte legen das Feld "Einrichtung" auf "Einrichtung" fest \_ , was auf einen Schnittstellen Methoden Fehler hinweist.

Allgemeine Einrichtungs Felder werden in der folgenden Tabelle beschrieben.



| Feld "Einrichtung"                | Wert        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einrichtung \_ der Anlage<br/> | 2<br/> | Für Fehler bei der **IDispatch** -Schnittstelle mit späterer Bindung. <br/>                                                                                                                                                                                                                                                             |
| Einrichtung \_ der Einrichtung<br/>      | 4<br/> | Für die meisten Statuscodes, die von Schnittstellen Methoden zurückgegeben werden. Die tatsächliche Bedeutung des Fehlers wird von der-Schnittstelle definiert. Das heißt, dass zwei **HRESULT**-s mit exakt demselben 32-Bit-Wert, der von zwei verschiedenen Schnittstellen zurückgegeben wurde, möglicherweise eine andere Bedeutung haben <br/>                                                       |
| Einrichtung \_ null<br/>     | 0<br/> | Für allgemein anwendbare allgemeine Statuscodes, z \_ . b. "OK". <br/>                                                                                                                                                                                                                                                    |
| Einrichtung von \_ RPC<br/>      | 1<br/> | Für von Remote Prozedur aufrufen zurückgegebene Statuscodes. <br/>                                                                                                                                                                                                                                                       |
| Speicher für Einrichtungen \_<br/>  | 3<br/> | Für Statuscodes, die von [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -oder [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Methoden aufrufen im Zusammenhang mit strukturierter Speicherung zurückgegeben werden Status Codes, deren Code (niedrigere 16 Bits) im Bereich der MS-DOS-Fehlercodes (d. h. kleiner als 256) liegt, haben dieselbe Bedeutung wie der entsprechende MS-DOS-Fehler. <br/> |
| Einrichtung von \_ Win32<br/>    | 7<br/> | Wird verwendet, um eine Möglichkeit zur Behandlung von Fehlercodes aus Funktionen in der Windows-API als **HRESULT** bereitzustellen. Fehlercodes in 16-Bit-OLE, die doppelte Systemfehler Codes aufweisen, wurden ebenfalls in die Win32-Anlage geändert \_ . <br/>                                                                                                 |
| Betriebs \_ Fenster<br/>  | 8<br/> | Wird für zusätzliche Fehlercodes von von Microsoft definierten Schnittstellen verwendet.<br/>                                                                                                                                                                                                                                            |



 

Das Feld Code ist eine eindeutige Zahl, die zum Darstellen des Fehlers oder der Warnung zugewiesen wird.

Gemäß der Konvention weisen **HRESULT** -Werte im allgemeinen Namen im folgenden Format auf: Ursache für den \_ *Schweregrad* des Standorts \_ .

Die *Einrichtung* ist entweder der Name der Einrichtung oder ein anderer Bezeichner. Der *Schweregrad* ist ein einzelner Buchstabe, e oder e, der angibt, ob der Funktions Rückruf erfolgreich war oder einen Fehler erzeugt hat (e). und *reason* ist ein Bezeichner, der die Bedeutung des Codes beschreibt. Beispielsweise gibt der Statuscode STG \_ E \_ fileotfound an, dass ein Speicher bezogener Fehler aufgetreten ist. insbesondere ist eine angeforderte Datei nicht vorhanden. Status Codes von Anlage \_ null lassen das *Einrichtungs* \_ Präfix aus.

Fehlercodes werden innerhalb des Kontexts einer Schnittstellen Implementierung definiert. Nach der Definition können Erfolgs Codes nicht mehr geändert oder neue Erfolgs Codes hinzugefügt werden. Es können jedoch neue Fehlercodes geschrieben werden. Microsoft behält sich das Recht vor, neue Fehlercodes (aber keine Erfolgs Codes) für die Schnittstellen zu definieren, die in der Einrichtung der Einrichtung \_ oder in neuen Einrichtungen beschrieben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](error-handling-in-com.md)
</dt> <dt>

[Windows-Protokolle: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

