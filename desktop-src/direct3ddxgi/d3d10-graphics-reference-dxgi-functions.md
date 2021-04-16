---
description: Dieser Abschnitt enthält Informationen zu den Funktionen, die von DXGI bereitgestellt werden.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: DXGI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520875"
---
# <a name="dxgi-functions"></a>DXGI-Funktionen

Dieser Abschnitt enthält Informationen zu den Funktionen, die von DXGI bereitgestellt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatedxgifactory"**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Erstellt eine DXGI 1,0-Factory, die Sie verwenden können, um andere DXGI-Objekte zu generieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Erstellt eine DXGI 1,1-Factory, die Sie verwenden können, um andere DXGI-Objekte zu generieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Erstellt eine DXGI 1,3-Factory, die Sie verwenden können, um andere DXGI-Objekte zu generieren.<br/> In Windows 8 würde jede DXGI-Factory, die erstellt wurde, während DXGIDebug.dll im System vorhanden war, Sie laden und verwenden. Ab Windows 8.1 fordern apps explizit an, dass Sie stattdessen laden DXGIDebug.dll. Verwenden Sie [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) , und geben Sie das DXGI- \_ \_ \_ Debugflag Create Factory an, um DXGIDebug.dll anzufordern. die dll wird geladen, wenn Sie auf dem System vorhanden ist.<br/> |
| [**Dxgideclareadapterremovalsupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Ermöglicht einem Prozess, anzugeben, dass er für alle zu entfernenden Grafikgeräte robust ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Dxgigetdebug-Schnittstelle**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Ruft eine Debugschnittstelle ab.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | Ruft eine Schnittstelle ab, die Windows Store-Apps zum Debuggen der Microsoft DirectX Graphics Infrastructure (DXGI) verwenden.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI-Referenz](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




