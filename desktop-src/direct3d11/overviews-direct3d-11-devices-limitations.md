---
title: Einschränkungen beim Erstellen von Warp-und Referenz Geräten
description: Zum Erstellen von Warp-und Referenz Geräten in Direct3D 10,1 und Direct3D 11,0 sind einige Einschränkungen vorhanden. Diese Einschränkungen werden in diesem Thema erläutert.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315195"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Einschränkungen beim Erstellen von Warp-und Referenz Geräten

Zum Erstellen von Warp-und Referenz Geräten in Direct3D 10,1 und Direct3D 11,0 sind einige Einschränkungen vorhanden. Diese Einschränkungen werden in diesem Thema erläutert.

Die \_ Treiber Typen "d3d10 Driver \_ Type Warp" und " \_ d3d10 \_ Driver \_ Type Reference" \_ werden auf der d3d10 \_ Feature \_ Level \_ 9 \_ 1 bis d3d10 \_ Feature \_ Level \_ 9 \_ 3 Feature Levels in Direct3D 10,1 nicht unterstützt. Außerdem wird der D3D \_ Driver \_ Type \_ Warp Driver Type auf D3D \_ Feature \_ Level \_ 11 \_ 0 in Direct3D 11,0 nicht unterstützt. Das heißt, wenn Sie [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) zum Erstellen eines Direct3D 10,1-Geräts oder zum Erstellen von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) zum Erstellen eines Direct3D 11,0-Geräts aufruft, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einer dieser Funktionsebenen im-Befehl angeben, ist der-Befehl ungültig. Für Warp-und Referenzgeräte sind nur die folgenden Kombinationen von featureebenen, Runtimes und Treiber Typen gültig:

-   D3D \_ Driver \_ Type \_ Warp on all Feature Levels in Direct3D 11,1 (in Windows 8 enthalten)

    D3D \_ Driver \_ Type \_ Reference on all Feature Levels in Direct3D 11,1

    Wenn Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) zum Erstellen eines Direct3D 11,1-Geräts aufzurufen, ist der-Befehl gültig, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einem dieser featureebenen angeben.

-   D3D \_ Driver \_ Type \_ Warp on D3D \_ Feature \_ Level \_ 9 \_ 1 bis D3D \_ Feature \_ Level \_ 10 \_ 1 Feature Levels in Direct3D 11

    D3D \_ Driver \_ Type \_ Reference on D3D \_ Feature \_ Level \_ 9 \_ 1 bis D3D \_ Feature \_ Level \_ 11 \_ 0 Feature Levels in Direct3D 11

    Wenn Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) zum Erstellen eines Direct3D 11-Geräts aufzurufen, ist der-Befehl gültig, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einem dieser featureebenen angeben.

-   D3d10 \_ Driver \_ Type \_ Warp and d3d10 \_ Driver \_ Type \_ Reference on d3d10 \_ Feature \_ Level \_ 10 \_ 0 through d3d10 \_ Feature \_ Level \_ 10 \_ 1 Feature Levels in Direct3D 10,1

    Wenn Sie [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) zum Erstellen eines Direct3D 10,1-Geräts aufzurufen, ist der-Befehl gültig, wenn Sie eine Kombination aus einem dieser Treiber Typen mit einem dieser featureebenen angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Einführung in Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Vorgehensweise: Erstellen eines Warp-Geräts](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Vorgehensweise: Erstellen eines Referenz Geräts](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**D3d10 \_ - \_ Treibertyp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3d10- \_ Funktion \_ Level1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**D3D \_ - \_ Treibertyp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**D3D \_ - \_ Featureebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 