---
description: Erstellt einen Gerätekontext (DC) für die angegebene Oberfläche.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: NtGdiDdGetDC-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 200635ca71ab16a84a137f85be13cc4fdbb6db200e4c0da795d07f945f06e9f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053340"
---
# <a name="ntgdiddgetdc-function"></a>NtGdiDdGetDC-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Erstellt einen Gerätekontext (DC) für die angegebene Oberfläche.

## <a name="syntax"></a>Syntax


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für eine DirectDraw-Oberfläche im Kernelmodus, die zuvor von [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) oder [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)zurückgegeben wurde.

</dd> <dt>

*puColorTable* \[ In\]
</dt> <dd>

Zeiger auf eine Überschreibungsfarbtabelle für den zurückgegebenen DC.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt diese Funktion einen gültigen **HDC** zurück. Andernfalls wird **NULL** zurückgegeben.

## <a name="remarks"></a>Hinweise

Pro Oberfläche ist jeweils nur ein Domänencontroller zulässig. Nachfolgende Aufrufe von **NtGdiDdGetDC** schlagen fehl, bis der vorherige DC freigegeben wurde.

Anwendungen wird empfohlen, stattdessen [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) aufzurufen, das die gleiche Funktionalität unabhängig vom Betriebssystem bereitstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
