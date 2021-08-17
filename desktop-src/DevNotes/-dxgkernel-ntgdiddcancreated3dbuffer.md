---
description: Bestimmt, ob der Treiber einen Befehl auf Treiberebene oder einen Scheitelpunktpuffer der angegebenen Beschreibung erstellen kann.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: NtGdiDdCanCreateD3DBuffer-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 777d22347c6a922407ef423a076ab3c1f876854b6c3aaf6aee7394aa3480f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956729"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a>NtGdiDdCanCreateD3DBuffer-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Bestimmt, ob der Treiber einen Befehl auf Treiberebene oder einen Scheitelpunktpuffer der angegebenen Beschreibung erstellen kann.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für die [**DD \_ DIRECTDRAW \_ GLOBAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) die das DirectDraw-Objekt darstellt.

</dd> <dt>

*puCanCreateSurfaceData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ CANCREATESURFACEDATA-Struktur.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) Diese Struktur enthält die Informationen, die der Treiber benötigt, um zu bestimmen, ob ein Befehls- oder Scheitelpunktpuffer erstellt werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdCanCreateD3DBuffer gibt** einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DDHAL-TREIBER \_ BEHANDELT**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
