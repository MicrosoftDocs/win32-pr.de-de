---
title: Shnittstellen der Debugschicht
description: Die folgenden Schnittstellen werden in d3d12sdklayers. h deklariert.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "106340482"
---
# <a name="debug-layer-interfaces"></a>Debug-ebenenschnittstellen

Die folgenden Schnittstellen sind in definiert `d3d12sdklayers.h` .

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**ID3D12Debug**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Eine Debug-Schnittstelle steuert Debugeinstellungen und überprüft den Pipeline Zustand. Sie kann nur verwendet werden, wenn die debugschicht aktiviert ist. |
| [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Fügt der debugschicht die GPU-basierte Validierung und die Synchronisierung der abhängigen Befehls Warteschlange hinzu. |
| [**ID3D12Debug2**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Fügt konfigurierbare Ebenen GPU-Based Validierung hinzu. |
| [**ID3D12Debug3**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Fügt der GPU-basierten Überprüfung der debugschicht, der abhängigen Befehls Warteschlangen-Synchronisierung und konfigurierbaren Ebenen der GPU-basierten Validierung hinzu. |
| [**ID3D12DebugCommandList**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Stellt Methoden zum Überwachen und Debuggen einer Befehlsliste bereit. |
| [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Diese Schnittstelle ermöglicht die Änderung zusätzlicher debugebeneneinstellungen der Befehlsliste. |
| [**ID3D12DebugCommandQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Bietet Methoden zum Überwachen und Debuggen einer Befehls Warteschlange. |
| [**ID3D12DebugDevice**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Diese Schnittstelle stellt ein Grafikgerät zum Debuggen dar. |
| [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Gibt Geräte weite debugebeneneinstellungen an. |
| [**ID3D12InfoQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Eine Informations Warteschlangen Schnittstelle speichert, ruft Debugmeldungen ab und filtert sie. Die Warteschlange besteht aus einer Nachrichten Warteschlange, einem optionalen Speicher Filter Stapel und einem optionalen Abruf Filter Stapel. |
| [**ID3D12SharingContract**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Teil eines Vertrags zwischen D3D11On12-Diagnose Ebenen und Grafik Diagnosetools. |

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichtung der Direct3D 12-Programmierungsumgebung](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referenz der Debugschicht](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referenz für Direct3D 12](direct3d-12-reference.md)
</dt> </dl>