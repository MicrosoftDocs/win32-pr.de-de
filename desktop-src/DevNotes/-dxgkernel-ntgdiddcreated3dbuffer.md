---
description: Wird zum Erstellen eines Befehls oder Scheitelpunktpuffers auf Treiberebene der angegebenen Beschreibung verwendet.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: NtGdiDdCreateD3DBuffer-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 55e28e50f10ced5380685cbdb5016363a77adc7e61d2df201565d18f4794fcf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956699"
---
# <a name="ntgdiddcreated3dbuffer-function"></a>NtGdiDdCreateD3DBuffer-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Wird zum Erstellen eines Befehls oder Scheitelpunktpuffers auf Treiberebene der angegebenen Beschreibung verwendet.

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

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für die [**DD \_ DIRECTDRAW \_ GLOBAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) die den Treiber darstellt.

</dd> <dt>

*hSurface* \[ in, out\]
</dt> <dd>

Zeiger auf ein Array von Oberflächenhandles. Der Aufrufer kann diese Handles auf die vorherigen Handlewerte festlegen, wenn die Oberflächen nach einem Moduswechsel neu erstellt werden. Dieser Prozess wird in der DirectDraw-Dokumentation als "Wiederherstellen" bezeichnet.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DDSURFACEDESC-Struktur,**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) die die Oberfläche oder den Puffer beschreibt, die der Treiber erstellen soll.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**globale DD \_ \_ SURFACE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) die Oberflächendaten enthält, die global für mehrere Oberflächen freigegeben werden.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Zeiger auf eine Liste von [**DD \_ SURFACE \_ LOCAL-Strukturen,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die vom Treiber erstellten Oberflächenobjekte beschreiben. In diesem Array ist in der Regel nur ein Eintrag zu finden.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ SURFACE \_ MORE-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) die zusätzliche lokale Oberflächendaten enthält.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ CREATESURFACEDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) die die zum Erstellen des Puffers erforderlichen Informationen enthält.

</dd> <dt>

*puhSurface* \[ in, out\]
</dt> <dd>

Wird von der DirectDraw-API verwendet und sollte nicht vom Treiber ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdCreateD3DBuffer gibt** einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DDHAL-TREIBER \_ BEHANDELT**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
