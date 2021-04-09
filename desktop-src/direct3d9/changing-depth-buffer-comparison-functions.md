---
description: Wenn tiefen Tests auf einer Renderingoberfläche durchgeführt werden, aktualisiert das Direct3D-System standardmäßig die Renderziel-Oberfläche, wenn der entsprechende tiefen Wert (z oder w) für jeden Punkt kleiner ist als der Wert im tiefen Puffer.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Ändern von tiefen Puffer Vergleichsfunktionen (d3d9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749064"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a>Ändern von tiefen Puffer Vergleichsfunktionen (d3d9)

Wenn tiefen Tests auf einer Renderingoberfläche durchgeführt werden, aktualisiert das Direct3D-System standardmäßig die Renderziel-Oberfläche, wenn der entsprechende tiefen Wert (z oder w) für jeden Punkt kleiner ist als der Wert im tiefen Puffer. In einer C++-Anwendung ändern Sie, wie das Systemvergleiche für tiefen Werte durchführt, indem Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/desktop/api) -Methode aufrufen, wobei der *State* -Parameter auf D3DRS \_ zfunc festgelegt ist. Der *value* -Parameter muss auf einen Wert im [**D3DCMPFUNC**](./d3dcmpfunc.md) -enumerierten Typ festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 
