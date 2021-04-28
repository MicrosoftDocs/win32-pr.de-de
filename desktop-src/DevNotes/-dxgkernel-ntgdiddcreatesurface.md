---
description: 'NtGdiDdCreateSurface-Funktion: Fügt eine Oberfläche an eine andere Oberfläche an.'
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: NtGdiDdCreateSurface-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085778"
---
# <a name="ntgdiddcreatesurface-function"></a>NtGdiDdCreateSurface-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Fügt eine Oberfläche an eine andere Oberfläche an.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für die [**DD \_ DIRECTDRAW \_ GLOBAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) die den Treiber darstellt.

</dd> <dt>

*hSurface* \[ In\]
</dt> <dd>

Vorheriges Handle für dieselbe Oberfläche. Wird verwendet, wenn die Oberfläche nach einem Moduswechsel neu erstellt wird.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Zeiger auf die [**DDSURFACEDESC-Struktur,**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) die die Oberfläche oder den Puffer beschreibt, die der Treiber erstellen soll.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Zeiger auf die [**GLOBALE DD \_ \_ SURFACE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) die Oberflächendaten enthält, die global mit mehreren Oberflächen gemeinsam genutzt werden.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Zeiger auf eine Liste von [**DD \_ SURFACE \_ LOCAL-Strukturen,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die vom Treiber erstellten Oberflächenobjekte beschreiben.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ SURFACE \_ MORE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) die zusätzliche lokale Oberflächendaten enthält.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ CREATESURFACEDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) die die zum Erstellen einer Oberfläche erforderlichen Informationen enthält.

</dd> <dt>

*puhSurface* \[ out\]
</dt> <dd>

Wird von der DirectDraw-API verwendet und darf nicht vom Treiber ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdCreateSurface** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK lautet, wird DirectDraw oder Direct3D mit der -Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Ihre Anwendung [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) aufruft, anstatt diese Funktion zu verwenden.

Beim Erstellen einer Kette von angefügten Oberflächen, z. B. einer Verkettung oder Kette oder Mipmaps, sollte [**ntGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) zuerst für jede Oberfläche aufgerufen werden. Rufen Sie dann [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) auf, um sie anzufügen. Rufen Sie schließlich **NtGdiDdCreateSurface** nur für die erste Oberfläche in der Kette auf. In diesem Fall ist *hSurface* das Handle, das von **NtGdiDdCreateSurfaceObject** für die erste Oberfläche in der Kette zurückgegeben wird.

**NtGdiDdCreateSurface** sollte nur aufgerufen werden, um Oberflächen im lokalen und nicht lokalen Videospeicher zu erstellen. Es sollte nie aufgerufen werden, um Systemspeicheroberflächen zu erstellen. Verwenden Sie stattdessen [**NtGdiDdCreateSurfaceObject,**](-dxgkernel-ntgdiddcreatesurfaceobject.md) um Systemspeicheroberflächen zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
