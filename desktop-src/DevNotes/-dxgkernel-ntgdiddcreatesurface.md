---
description: Fügt eine Oberfläche an eine andere Oberfläche an.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Ntgdiddkreatesurface-Funktion (ntgdi. h)
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
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125947"
---
# <a name="ntgdiddcreatesurface-function"></a>Ntgdiddkreatesurface-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

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

*hdirectdraw* \[ in\]
</dt> <dd>

Handle zur [**globalen DD \_ DirectDraw \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die den Treiber darstellt.

</dd> <dt>

*hsurface* \[ in\]
</dt> <dd>

Vorheriges Handle für dieselbe Oberfläche. Wird verwendet, wenn die Oberfläche nach einem Modusschalter neu erstellt wird.

</dd> <dt>

*pusurfacedescription* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die [**ddsurfacedebug**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) -Struktur, die die vom Treiber zu erstellende Oberfläche oder den Puffer beschreibt.

</dd> <dt>

*pusurfakeglobaldata* \[ in, out\]
</dt> <dd>

Ein Zeiger auf [**die \_ \_ globale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) Struktur, die Oberflächendaten enthält, die Global mit mehreren Oberflächen gemeinsam genutzt werden.

</dd> <dt>

*pusurfakelocaldata* \[ in, out\]
</dt> <dd>

Zeiger auf eine Liste von [**\_ \_ lokalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) TT-Oberflächenstrukturen, die die vom Treiber erstellten Oberflächen Objekte beschreiben.

</dd> <dt>

*pusurfakemoredata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD- \_ Oberfläche \_ mehr**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) Struktur, die zusätzliche lokale Oberflächendaten enthält.

</dd> <dt>

*pukreatesurfacedata* \[ in, out\]
</dt> <dd>

Zeiger auf eine DD-Struktur von " [**\_ foatesurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) ", die die zum Erstellen einer Oberfläche erforderlichen Informationen enthält.

</dd> <dt>

*puhsurface* \[ vorgenommen\]
</dt> <dd>

Wird von der DirectDraw-API verwendet und sollte nicht vom Treiber ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddkreatesurface** gibt einen der folgenden Rückruf Codes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ddhal- \_ Treiber \_ behandelt**</dt> </dl>    | Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**ddhal- \_ Treiber \_ nothandled**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Ihre Anwendung [IDirectDraw7:: | atesurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) aufruft, anstatt diese Funktion zu verwenden.

Beim Erstellen einer Kette angefügter Oberflächen, z. b. einer Swapkette oder einer Kette oder von Mipmaps, sollte [**ntgdiddkreatesurfaceobject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) zuerst für jede Oberfläche aufgerufen werden. Anschließend wird [**ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md) aufgerufen, um sie anzufügen. Nennen Sie schließlich **ntgdiddkreatesurface** nur für die erste Oberfläche in der Kette. In diesem Fall wäre *hsurface* das Handle, das von **ntgdiddkreatesurfaceobject** für die erste Oberfläche in der Kette zurückgegeben wird.

**Ntgdiddkreatesurface** sollte nur aufgerufen werden, um Oberflächen in lokalem und nicht lokalem Videospeicher zu erstellen. Es sollte nie aufgerufen werden, um Systemspeicher Oberflächen zu erstellen. Verwenden Sie stattdessen [**ntgdiddkreatesurfaceobject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) , um Systemspeicher Oberflächen zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
