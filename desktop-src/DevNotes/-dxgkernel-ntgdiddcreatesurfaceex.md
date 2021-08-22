---
description: Erstellt eine Microsoft Direct3D-Oberfläche aus einer Microsoft DirectDraw-Oberfläche und ordnet ihr einen angeforderten Handlewert zu.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: NtGdiDdCreateSurfaceEx-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: ff5db8859cc339dc97f86e1b0421f662d69b85ba0f46449a1e721c1dc355d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956559"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>NtGdiDdCreateSurfaceEx-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Erstellt eine Microsoft Direct3D-Oberfläche aus einer Microsoft DirectDraw-Oberfläche und ordnet ihr einen angeforderten Handlewert zu.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für das DirectDraw-Objekt, das von der Anwendung erstellt wurde.

</dd> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für die DirectDraw-Oberfläche, die für Direct3D erstellt werden soll. Diese Handles sind innerhalb der einzelnen [**DD \_ DIRECTDRAW \_ LOCAL-Strukturen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) eindeutig.

</dd> <dt>

*dwSurfaceHandle* \[ In\]
</dt> <dd>

Handle für eine [**DD \_ CREATESURFACEEXDATA-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) die die Informationen enthält, die der Treiber zum Erstellen der Oberfläche benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdCreateSurfaceEx gibt** einen der folgenden Rückrufcodes zurück.



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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
