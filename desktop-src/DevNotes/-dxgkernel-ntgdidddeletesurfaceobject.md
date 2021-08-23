---
description: NtGdiDdDeleteSurfaceObject löscht ein zuvor erstelltes Oberflächenobjekt im Kernelmodus.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: NtGdiDdDeleteSurfaceObject-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73418993e549bc3a72f1f4bc953b4f177a4b413d62f03e0c6e8b0c58b35998e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956529"
---
# <a name="ntgdidddeletesurfaceobject-function"></a>NtGdiDdDeleteSurfaceObject-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

**NtGdiDdDeleteSurfaceObject** löscht ein zuvor erstelltes Oberflächenobjekt im Kernelmodus.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für das zuvor erstellte Kernelmodusoberflächenobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dies erfolgreich ist, gibt diese Funktion **TRUE zurück.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Anwendungen wird empfohlen, die DirectDraw- und [Direct3D-APIs zum](../direct3d10/d3d10-graphics-reference.md) Erstellen und Verwalten von Grafikgeräteobjekten zu verwenden. Diese Konstrukte abstrahieren den Prozess der Geräteerstellung auf vereinfachte und betriebssystemunabhängige Weise.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdDeleteSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
