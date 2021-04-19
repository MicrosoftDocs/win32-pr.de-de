---
description: Viele C++-Anwendungen löschen den tiefen Puffer, bevor Sie jeden neuen Frame rendern.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Löschen von tiefen Puffern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344827"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Löschen von tiefen Puffern (Direct3D 9)

Viele C++-Anwendungen löschen den tiefen Puffer, bevor Sie jeden neuen Frame rendern. Sie können den tiefen Puffer über Direct3D explizit löschen, indem Sie [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) aufrufen und D3DCLEAR \_ ZBuffer für den flags-Parameter angeben. Mit der **IDirect3DDevice9:: Clear** -Methode können Sie einen beliebigen tiefen Wert im Z-Parameter angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 
