---
description: Standardmäßig ist es dem Direct3D-System gestattet, in den tiefen Puffer zu schreiben. Bei den meisten Anwendungen wird das Schreiben in den tiefen Puffer aktiviert, aber Sie können einige besondere Effekte erzielen, indem Sie dem Direct3D-System nicht gestatten, in den tiefen Puffer zu schreiben.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Ändern des Schreibzugriffs auf den Lesezugriff (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339688"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>Ändern des Schreibzugriffs auf den Lesezugriff (Direct3D 9)

Standardmäßig ist es dem Direct3D-System gestattet, in den tiefen Puffer zu schreiben. Bei den meisten Anwendungen wird das Schreiben in den tiefen Puffer aktiviert, aber Sie können einige besondere Effekte erzielen, indem Sie dem Direct3D-System nicht gestatten, in den tiefen Puffer zu schreiben.

Sie können tiefe Puffer Schreibvorgänge in C++ deaktivieren, indem Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode aufrufen, wobei der State-Parameter auf D3DRS \_ zbeschreib teenable und der value-Parameter auf 0 festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 
