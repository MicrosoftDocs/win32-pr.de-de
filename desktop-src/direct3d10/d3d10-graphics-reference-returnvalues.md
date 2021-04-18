---
description: In der folgenden Tabelle sind Rückgabecodes von API-Funktionen enthalten.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Direct3D 10-Rückgabe Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340116"
---
# <a name="direct3d-10-return-codes"></a>Direct3D 10-Rückgabe Codes

In der folgenden Tabelle sind Rückgabecodes von API-Funktionen enthalten.



| HRESULT                                         | BESCHREIBUNG                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10- \_ Fehler \_ Datei \_ nicht \_ gefunden.                  | Die Datei wurde nicht gefunden.                                                                                                                               |
| D3d10 \_ Fehler \_ zu \_ viele \_ eindeutige \_ Zustands \_ Objekte | Es sind zu viele eindeutige Instanzen eines bestimmten [Zustands Objekt](d3d10-graphics-programming-guide-api-features-state-objects.md)Typs vorhanden.          |
| D3DERR \_ invalidcall                             | Der Methoden Aufrufwert ist ungültig. Beispielsweise ist der-Parameter einer Methode möglicherweise kein gültiger Zeiger.                                                             |
| D3DERR \_ wasstilldrawing                         | Der vorherige Blit-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.                                                   |
| E \_ fehlschlagen                                         | Es wurde versucht, ein Gerät mit aktivierter [debugschicht](d3d10-graphics-programming-guide-api-features-layers.md) zu erstellen, und die Ebene ist nicht installiert. |
| E \_ invalidArg                                   | An die Rückgabe Funktion wurde ein ungültiger Parameter übergeben.                                                                                            |
| E \_ outo-Memory                                  | Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den-Vorgang abzuschließen.                                                                                   |
| E \_ notimpl                                      | Der Methodenaufrufe wird nicht mit der übergebenen Parameter Kombination implementiert.                                                                              |
| S \_ false                                        | Alternativer Erfolgs Wert, der einen erfolgreichen, aber nicht dem Standard entsprechende Abschluss angibt (die genaue Bedeutung hängt vom Kontext ab).                                 |
| S \_ OK                                           | Kein Fehler ist aufgetreten.                                                                                                                                    |



 

Um Code zu schreiben, der die [HRESULT-Werte](../winprog/windows-data-types.md) robuster verarbeitet, verwenden Sie die Makros erfolgreich (HR) und failed (HR).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Referenz](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Referenz für Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
