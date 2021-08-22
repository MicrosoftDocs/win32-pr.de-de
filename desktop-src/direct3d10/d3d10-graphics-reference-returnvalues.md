---
description: Die folgende Tabelle enthält Rückgabecodes von API-Funktionen.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Direct3D 10-Rückgabecodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c7e7bca25d240bf7775a6f4d6476148e3749e283ab4f8fb3511bf8b53bb711
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282800"
---
# <a name="direct3d-10-return-codes"></a>Direct3D 10-Rückgabecodes

Die folgende Tabelle enthält Rückgabecodes von API-Funktionen.



| HRESULT                                         | Beschreibung                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10-FEHLERDATEI \_ \_ NICHT \_ \_ GEFUNDEN                  | Die Datei wurde nicht gefunden.                                                                                                                               |
| D3D10-FEHLER: \_ ZU VIELE EINDEUTIGE \_ \_ \_ \_ \_ ZUSTANDSOBJEKTE | Es gibt zu viele eindeutige Instanzen eines bestimmten [Zustandsobjekttyps.](d3d10-graphics-programming-guide-api-features-state-objects.md)          |
| D3DERR \_ INVALIDCALL                             | Der Methodenaufruf ist ungültig. Beispielsweise kann der Parameter einer Methode kein gültiger Zeiger sein.                                                             |
| D3DERR \_ WAS BEGDRAWING                         | Der vorherige Blit-Vorgang, bei dem Informationen auf oder von dieser Oberfläche übertragen werden, ist unvollständig.                                                   |
| E \_ FAIL                                         | Es wurde versucht, ein Gerät mit aktivierter [Debugebene](d3d10-graphics-programming-guide-api-features-layers.md) zu erstellen, und die Ebene ist nicht installiert. |
| E \_ INVALIDARG                                   | Ein ungültiger Parameter wurde an die zurückgebende Funktion übergeben.                                                                                            |
| E \_ OUTOFMEMORY                                  | Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den Aufruf abschließen zu können.                                                                                   |
| E \_ NOTIMPL                                      | Der Methodenaufruf wird nicht mit der übergebenen Parameterkombination implementiert.                                                                              |
| S \_ FALSE                                        | Alternativer Erfolgswert, der eine erfolgreiche, aber nicht standardmäßige Vervollständigung angibt (die genaue Bedeutung hängt vom Kontext ab).                                 |
| S \_ OK                                           | Kein Fehler ist aufgetreten.                                                                                                                                    |



 

Verwenden Sie die Makros SUCCEEDED(hr) und FAILED(hr), um Code zu schreiben, der [HRESULT-Werte](../winprog/windows-data-types.md) robust verarbeitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Referenz](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Referenz zu Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
