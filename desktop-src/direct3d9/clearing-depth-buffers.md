---
description: Viele C++-Anwendungen löschen den Tiefenpuffer, bevor sie jeden neuen Frame rendern.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Löschen von Tiefenpuffern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989310"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Löschen von Tiefenpuffern (Direct3D 9)

Viele C++-Anwendungen löschen den Tiefenpuffer, bevor sie jeden neuen Frame rendern. Sie können den Tiefenpuffer explizit über Direct3D löschen, indem Sie [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) aufrufen und D3DCLEAR \_ ZBUFFER für den Flags-Parameter angeben. Mit **der IDirect3DDevice9::Clear-Methode** können Sie einen beliebigen Tiefenwert im Z-Parameter angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefenpuffer](depth-buffers.md)
</dt> </dl>

 

 
