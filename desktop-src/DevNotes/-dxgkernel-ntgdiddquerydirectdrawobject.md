---
description: Fragt eine zuvor erstellte Kernel Modus-Darstellung eines Microsoft DirectDraw-Objekts für seine Funktionen ab.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Ntgdiddquerydirectdrawobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861475"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>Ntgdiddquerydirectdrawobject-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Fragt eine zuvor erstellte Kernel Modus-Darstellung eines Microsoft DirectDraw-Objekts für seine Funktionen ab.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdrawlocal* \[ in\]
</dt> <dd>

Handle für den zuvor erstellten Kernel Modus-DirectDraw-Gerät.

</dd> <dt>

*phalinfo* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) -Struktur, die mit den Funktionen des Geräts gefüllt wird. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*pcallbackflags* 
</dt> <dd>

Zeiger auf einen vom Aufrufer bereitgestellten Puffer, der die vom Treiber gemeldeten Rückruf Flags speichert. Der Puffer sollte die Größe 3 \* sizeof (DWORD) aufweisen und Rückruf Flags in der folgenden Reihenfolge speichern: pcallbackflags \[ 0 für Flags in TT-Rückrufen \] , pcallbackflags [**\_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks) \[ 1 \] für Flags in [**DD \_ surfakecallbacks**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)und pcallbackflags \[ 2 \] für Flags in [**DD \_ palettecallbacks**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puD3dCallbacks* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine Tabelle mit Direct3D-Rückruf Zeigern. Die Tabelle wird mit Zeigern auf Funktionen in Gdi32.dll gefüllt, die einen Direct3D-Anzeigetreiber imitieren. Diese Rückruf Tabelle ist identisch mit der D3DHAL \_ D3DCALLBACKS-Struktur, die in der DDK-Dokumentation erläutert wird.

</dd> <dt>

*puD3dDriverData* \[ vorgenommen\]
</dt> <dd>

Zeiger auf [**D3DHAL \_ globaldriverdata**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) -Daten, wie in der DDK-Dokumentation beschrieben.

</dd> <dt>

*puD3dBufferCallbacks* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine Tabelle mit Rückruf Zeigern. Die Tabelle wird mit Zeigern auf Funktionen in Gdi32.dll gefüllt, die einen Direct3D-Anzeigetreiber imitieren. Diese Rückruf Tabelle ist identisch mit der ddhal \_ dbxebufcallbacks-Struktur, die der in der DDK-Dokumentation erörterten [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) -Struktur zugeordnet ist, mit dem Unterschied, dass Member XxxD3DBuffer in **DD \_ D3DBUFCALLBACKS** durch xxxexecutebuffer in ddhal \_ DDE xebufcallbacks ersetzt werden.

</dd> <dt>

*puD3dTextureFormats* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von [**ddsurfacede SC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) -Strukturen, die den Satz zulässiger Textur Formate definieren.

</dd> <dt>

*punüberheaps* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den **dwnumheaps** -Member von [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmidata**. Der **dwnumheaps** -Member gibt die Anzahl der Arbeitsspeicher Heaps in *puvmlist* an. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puvmlist* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine Liste von Videospeicher-Heap Deskriptoren. Kann **null** sein. Dieser Parameter wird nicht verwendet, da die Videospeicher Verwaltung vollständig im Kernel Modus erfolgt.

</dd> <dt>

*punumschlag* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den **punumfourcccodes** -Member von [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddcaps**. Der **punenumfourcccodes** -Member gibt die Anzahl von [vier Zeichen Codes](../directshow/fourcc-codes.md) an, die vom Treiber unterstützt werden. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*pufourcc* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine Liste der unterstützten [viercc-Oberflächen Formate (vier Zeichen Codes)](../directshow/fourcc-codes.md) . Kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ein-Vorgang wurde in einem zweistufigen Prozess durchgeführt. Im ersten Schritt sollten *pufourcc*, *puvmlist* und *puD3dTextureFormats* **null** sein, und [**ddquerydirectdrawobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) wird [**DD \_ halinfo**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)ausfüllen.**ddcaps**. **dwnumfourcccodes**, **DD \_ halinfo**.**vmidata**. **dwnumheaps** und [**D3DHAL \_ globaldriverdata**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwnumtextureformats** mit der Anzahl der Einträge, die zurückgegeben werden sollen. Im zweiten Aufruf sollte der Aufrufer Arrays der angegebener Größe zuordnen und diese Zeiger anstelle von **null** -Werten in den Parametern " *pufourcc*", " *puvmlist* " und " *puD3dTextureFormats* " übergeben. Die Arrays werden dann mit den entsprechenden Daten aufgefüllt.

Anwendungen wird empfohlen, die DirectDraw-und [Direct3D](../direct3d10/d3d10-graphics-reference.md) -APIs zu verwenden, um Grafikgeräte Objekte zu erstellen und zu verwalten. Diese Konstrukte abstrahieren den Geräte Erstellungs Prozess auf vereinfachte und betriebssystemunabhängige Weise.

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

[**Ddquerydirectdrawobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**Ntgdiddkreatedirectdrawobject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
