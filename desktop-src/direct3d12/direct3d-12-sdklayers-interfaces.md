---
title: Shnittstellen der Debugschicht
description: Die folgenden Schnittstellen werden in d3d12sdungyers.h deklariert.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812877"
---
# <a name="debug-layer-interfaces"></a>Debugebenenschnittstellen

Die folgenden Schnittstellen sind in `d3d12sdklayers.h` definiert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Eine Debugschnittstelle steuert Debugeinstellungen und überprüft den Pipelinezustand. Sie kann nur verwendet werden, wenn die Debugebene aktiviert ist. |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Fügt der Debugebene GPU-basierte Validierung und Synchronisierung der Warteschlange für abhängige Befehle hinzu. |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Fügt konfigurierbare Ebenen der GPU-Based hinzu. |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Fügt der GPU-basierten Validierung auf Debugebene, der Synchronisierung der Warteschlange für abhängige Befehle und konfigurierbaren Ebenen der GPU-basierten Validierung hinzu. |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | Fügt die Möglichkeit zum Deaktivieren der Debugebene hinzu. |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | Fügt der Debugebene die Möglichkeit hinzu, die automatische Benennung von Objekten zu konfigurieren. |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Stellt Methoden zum Überwachen und Debuggen einer Befehlsliste zur Anwendung. |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Diese Schnittstelle ermöglicht die Änderung zusätzlicher Einstellungen für die Debugebene der Befehlsliste. |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Stellt Methoden zum Überwachen und Debuggen einer Befehlswarteschlange zur Anwendung. |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Diese Schnittstelle stellt ein Grafikgerät für das Debuggen dar. |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Gibt geräteweite Debugebeneneinstellungen an. |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Eine Information-Queue-Schnittstelle speichert Debugmeldungen, ruft sie ab und filtert sie. Die Warteschlange besteht aus einer Nachrichtenwarteschlange, einem optionalen Speicherfilterstapel und einem optionalen Abruffilterstapel. |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Teil eines Vertrags zwischen D3D11On12-Diagnoseebenen und Grafikdiagnosetools. |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichtung der Direct3D 12-Programmierungsumgebung](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referenz der Debugschicht](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>