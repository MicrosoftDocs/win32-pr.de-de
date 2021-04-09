---
description: Wird verwendet, um einen Befehl auf Treiber Ebene oder einen Vertex-Puffer der angegebenen Beschreibung zu erstellen.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: NtGdiDdCreateD3DBuffer-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958189"
---
# <a name="ntgdiddcreated3dbuffer-function"></a>NtGdiDdCreateD3DBuffer-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Wird verwendet, um einen Befehl auf Treiber Ebene oder einen Vertex-Puffer der angegebenen Beschreibung zu erstellen.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdraw* \[ in\]
</dt> <dd>

Handle zur [**globalen DD \_ DirectDraw \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) -Struktur, die den Treiber darstellt.

</dd> <dt>

*hsurface* \[ in, out\]
</dt> <dd>

Zeiger auf ein Array von Oberflächen Handles. Der Aufrufer kann diese Handles auf die vorherigen handle-Werte festlegen, wenn die Oberflächen nach einem Modusschalter neu erstellt werden. Dieser Vorgang wird in der DirectDraw-Dokumentation als "Wiederherstellen" bezeichnet.

</dd> <dt>

*pusurfacedescription* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**ddsurfacedebug**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) -Struktur, die die vom Treiber zu erstellende Oberfläche oder den Puffer beschreibt.

</dd> <dt>

*pusurfakeglobaldata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**\_ \_ globale**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) TT-Oberflächenstruktur, die Oberflächendaten enthält, die Global mit mehreren Oberflächen gemeinsam genutzt werden.

</dd> <dt>

*pusurfakelocaldata* \[ in, out\]
</dt> <dd>

Zeiger auf eine Liste von [**\_ \_ lokalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) TT-Oberflächenstrukturen, die die vom Treiber erstellten Oberflächen Objekte beschreiben. Es gibt in der Regel nur einen Eintrag in diesem Array.

</dd> <dt>

*pusurfakemoredata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD- \_ Oberfläche \_ mehr**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) Struktur, die zusätzliche lokale Oberflächendaten enthält.

</dd> <dt>

*pukreatesurfacedata* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine DD-Struktur von " [**\_ kreatesurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) ", die die zum Erstellen des Puffers erforderlichen Informationen enthält.

</dd> <dt>

*puhsurface* \[ in, out\]
</dt> <dd>

Wird von der DirectDraw-API verwendet und sollte nicht vom Treiber ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdCreateD3DBuffer** gibt einen der folgenden Rückruf Codes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ddhal- \_ Treiber \_ behandelt**</dt> </dl>    | Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**ddhal- \_ Treiber \_ nothandled**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.<br/> |



 

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

 

 
