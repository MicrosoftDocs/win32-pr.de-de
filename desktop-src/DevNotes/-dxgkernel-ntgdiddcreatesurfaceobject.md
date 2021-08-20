---
description: Erstellt ein Oberflächenobjekt im Kernelmodus, das das Benutzermodus-Oberflächenobjekt darstellt, auf das puSurfaceLocal verweist.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: NtGdiDdCreateSurfaceObject-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7dac10cb5f648cc7281d95bcd83be9983a63abd76208f6f745e1bd6c5ec00b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956539"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>NtGdiDdCreateSurfaceObject-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Erstellt ein Oberflächenobjekt im Kernelmodus, das das Benutzermodusoberflächenobjekt darstellt, auf das *puSurfaceLocal verweist.*

## <a name="syntax"></a>Syntax


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDrawLocal* \[ In\]
</dt> <dd>

Handle für das DirectDraw-Objekt im Kernelmodus.

</dd> <dt>

*hSurface* \[ In\]
</dt> <dd>

Vorheriges Handle auf derselben Oberfläche. Wird verwendet, wenn die Oberfläche nach einem Moduswechsel neu erstellt wird.

</dd> <dt>

*puSurfaceLocal* \[ In\]
</dt> <dd>

Zeiger auf die [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die das DirectDraw-Benutzermodusoberflächenobjekt darstellt, dem der zugeordnete Arbeitsspeicher zugeordnet werden soll. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puSurfaceMore* \[ In\]
</dt> <dd>

Zeiger auf die [**DD \_ SURFACE \_ MORE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) die zusätzliche lokale Daten für jedes einzelne Oberflächenobjekt enthält. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puSurfaceGlobal* \[ In\]
</dt> <dd>

Zeiger auf die [**globale DD \_ \_ SURFACE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) die Oberflächendaten enthält, die global mit mehreren Oberflächen gemeinsam genutzt werden. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*bVervollständigen* \[ In\]
</dt> <dd>

Kernelmodus-Objektvervollständigungsflag. Kann einer der folgenden Werte sein.

<dt>



 (TRUE)


</dt> <dd>

Schließen Sie die gesamte Verarbeitung in Bezug auf die Kernelmodusdarstellung ab.

</dd> <dt>



 (FALSE)


</dt> <dd>

Erstellen Sie das -Objekt, aber richten Sie keine internen Daten wie den Speicherzeiger ein. Objekte, die mit **FALSE** erstellt wurden, können mit [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) angefügt werden und werden durch einen Aufruf von [**NtGdiDdCreateSurface abgeschlossen.**](-dxgkernel-ntgdiddcreatesurface.md)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion ein Handle für die Darstellung der Kernelmodusoberfläche zurück. Andernfalls wird **NULL zurückgegeben.**

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
