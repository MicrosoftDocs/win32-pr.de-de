---
title: Direct3D 11-Rückgabecodes
description: Die Rückgabecodes von API-Funktionen.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d932c3ce3828f375e90bf322af6c42dc112b845f44dfe22f0d0988930129efea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990040"
---
# <a name="direct3d-11-return-codes"></a>Direct3D 11-Rückgabecodes

Gibt Codes von API-Funktionen zurück.

| HRESULT | Beschreibung |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | Die Datei wurde nicht gefunden. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Es gibt zu viele eindeutige Instanzen eines bestimmten Zustandsobjekttyps. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Es gibt zu viele eindeutige Instanzen eines bestimmten Ansichtsobjekttyps. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | Der erste Aufruf von [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) nach [**id3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) oder [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) pro Ressource wurde D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (ersetzt durch DXGI_ERROR_INVALID_CALL) (0x887A0001) | Der Methodenaufruf ist ungültig. Beispielsweise kann der Parameter einer Methode kein gültiger Zeiger sein. |
| D3DERR_WASSTILLDRAWING (ersetzt durch DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | Der vorherige Blit-Vorgang, bei dem Informationen auf oder von dieser Oberfläche übertragen werden, ist unvollständig. |
| E_FAIL (0x80004005) | Es wurde versucht, ein Gerät mit aktivierter Debugebene zu erstellen, und die Ebene ist nicht installiert. |
| E_INVALIDARG (0x80070057) | Ein ungültiger Parameter wurde an die zurückgebende Funktion übergeben. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D konnte nicht genügend Arbeitsspeicher zuordnen, um den Aufruf abschließen zu können. |
| E_NOTIMPL (0x80004001) | Der Methodenaufruf wird nicht mit der übergebenen Parameterkombination implementiert. |
| S_FALSE ((HRESULT)1L) | Alternativer Erfolgswert, der eine erfolgreiche, aber nicht standardmäßige Vervollständigung angibt (die genaue Bedeutung hängt vom Kontext ab). |
| S_OK ((HRESULT)0L) | Kein Fehler ist aufgetreten. |

Weitere Rückgabecodes finden Sie unter [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz für Direct3D 11](d3d11-graphics-reference.md)