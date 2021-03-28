---
title: Direct3D 11-Rückgabe Codes
description: Die Rückgabecodes von API-Funktionen.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4130ed07faaabfd24bb48454d4e450f307c7a12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039127"
---
# <a name="direct3d-11-return-codes"></a>Direct3D 11-Rückgabe Codes

Rückgabecodes von API-Funktionen.

| HRESULT | BESCHREIBUNG |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887c0002) | Die Datei wurde nicht gefunden. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887c0001) | Es sind zu viele eindeutige Instanzen eines bestimmten Zustands Objekt Typs vorhanden. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887c0003) | Es sind zu viele eindeutige Instanzen eines bestimmten Typs von Ansichts Objekt vorhanden. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887c0004) | Der erste Aufrufen von [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) nach [**ID3D11Device:: anatedeferredcontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) oder [**Verknüpfung id3d11devicecontext aus:: finishcommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) pro Ressource war nicht D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (durch DXGI_ERROR_INVALID_CALL ersetzt) (0x887a0001) | Der Methoden Aufrufwert ist ungültig. Beispielsweise ist der-Parameter einer Methode möglicherweise kein gültiger Zeiger. |
| D3DERR_WASSTILLDRAWING (durch DXGI_ERROR_WAS_STILL_DRAWING ersetzt) (0x887a000a) | Der vorherige Blit-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig. |
| E_FAIL (0x80004005) | Es wurde versucht, ein Gerät mit aktivierter debugschicht zu erstellen, und die Ebene ist nicht installiert. |
| E_INVALIDARG (0x80070057) | An die Rückgabe Funktion wurde ein ungültiger Parameter übergeben. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den-Vorgang abzuschließen. |
| E_NOTIMPL (0x80004001) | Der Methodenaufrufe wird nicht mit der übergebenen Parameter Kombination implementiert. |
| S_FALSE ((HRESULT) 1L) | Alternativer Erfolgs Wert, der einen erfolgreichen, aber nicht dem Standard entsprechende Abschluss angibt (die genaue Bedeutung hängt vom Kontext ab). |
| S_OK ((HRESULT) 0l) | Kein Fehler ist aufgetreten. |

Weitere Rückgabecodes finden Sie unter [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz für Direct3D 11](d3d11-graphics-reference.md)