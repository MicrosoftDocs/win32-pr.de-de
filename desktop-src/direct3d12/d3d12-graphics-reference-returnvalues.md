---
title: Direct3D 12-Rückgabecodes
description: Im folgenden finden Sie Rückgabecodes von API-Funktionen.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337458"
---
# <a name="direct3d-12-return-codes"></a>Direct3D 12-Rückgabecodes

Im folgenden finden Sie Rückgabecodes von API-Funktionen. Weitere Rückgabecodes finden Sie unter [DXGI \_ Error](/windows/desktop/direct3ddxgi/dxgi-error).



| HRESULT                                                                  | BESCHREIBUNG                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| D3D12- \_ Fehler \_ Adapter wurde \_ nicht \_ gefunden.                                        | Das angegebene zwischengespeicherte PSO wurde auf einem anderen Adapter erstellt und kann auf dem aktuellen Adapter nicht wieder verwendet werden.          |
| D3D12- \_ Fehler \_ Treiber \_ Version stimmen nicht \_ überein.                                  | Das angegebene zwischengespeicherte PSO wurde auf einer anderen Treiber Version erstellt und kann nicht auf dem aktuellen Adapter wieder verwendet werden.  |
| D3DERR \_ invalidcall(durch DXGI- \_ Fehler \_ ungültigen-Befehl ersetzt \_ )           | Der Methoden Aufrufwert ist ungültig. Beispielsweise ist der-Parameter einer Methode möglicherweise kein gültiger Zeiger.                             |
| D3DERR \_ wasstilldrawing (durch DXGI- \_ Fehler \_ ersetzt \_ ) wurde noch \_ gezeichnet. | Der vorherige Blit-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.                   |
| E \_ fehlschlagen                                                                  | Es wurde versucht, ein Gerät mit aktivierter debugschicht zu erstellen, und die Ebene ist nicht installiert.                             |
| E \_ invalidArg                                                            | An die Rückgabe Funktion wurde ein ungültiger Parameter übergeben.                                                             |
| E \_ outo-Memory                                                           | Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den-Vorgang abzuschließen.                                                   |
| E \_ notimpl                                                               | Der Methodenaufrufe wird nicht mit der übergebenen Parameter Kombination implementiert.                                               |
| S \_ false                                                                 | Alternativer Erfolgs Wert, der einen erfolgreichen, aber nicht dem Standard entsprechende Abschluss angibt (die genaue Bedeutung hängt vom Kontext ab). |
| S \_ OK                                                                    | Kein Fehler ist aufgetreten.                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 