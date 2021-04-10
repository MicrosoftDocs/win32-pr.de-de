---
description: Erstellt einen Gerätekontext (DC) für die angegebene Oberfläche.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Ntgdiddgetdc-Funktion (ntgdi. h)
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
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126752"
---
# <a name="ntgdiddgetdc-function"></a>Ntgdiddgetdc-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

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

*hsurface* \[ in\]
</dt> <dd>

Handle für eine DirectDraw-Oberfläche im Kernelmodus, die zuvor von [**ntgdiddkreatesurface**](-dxgkernel-ntgdiddcreatesurface.md) oder [**ntgdiddkreatesurfaceobject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)zurückgegeben wurde.

</dd> <dt>

*pucolortable* \[ in\]
</dt> <dd>

Zeiger auf eine Überschreibungs Farbtabelle für den zurückgegebenen DC.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Funktion einen gültigen **hdc** zurück. Andernfalls wird **null** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Pro Oberfläche ist jeweils nur ein DC zulässig. Bei nachfolgenden Aufrufen von **ntgdiddgetdc** tritt ein Fehler auf, bis der vorherige DC freigegeben wurde.

Anwendungen wird empfohlen, stattdessen [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) aufzurufen, wodurch die gleiche Funktionalität auf eine Weise unabhängig vom Betriebssystem bereitgestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**Ddgetdc**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
