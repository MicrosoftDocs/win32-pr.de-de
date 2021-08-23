---
description: Steuert die Leuchtdichte- und Helligkeitssteuerelemente einer Überlagerungsoberfläche.
ms.assetid: 2f617c89-5505-4d84-be7d-473b216c0571
title: NtGdiDdColorControl-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdColorControl
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5e83dba1dcdc46fb4715fbbdcb6a5ed009f77cf29212e65be9b0270ba01a55e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956709"
---
# <a name="ntgdiddcolorcontrol-function"></a>NtGdiDdColorControl-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Steuert die Leuchtdichte- und Helligkeitssteuerelemente einer Überlagerungsoberfläche.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdColorControl(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_COLORCONTROLDATA puColorControlData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für die [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die Überlagerungsoberfläche darstellt.

</dd> <dt>

*puColorControlData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ COLORCONTROLDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) die die Farbsteuerelementinformationen für eine angegebene Überlagerungsoberfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdColorControl** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
