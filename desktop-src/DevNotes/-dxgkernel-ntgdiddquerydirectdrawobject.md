---
description: Fragt eine zuvor erstellte Kernelmodusdarstellung eines Microsoft DirectDraw-Objekts nach seinen Funktionen ab.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: NtGdiDdQueryDirectDrawObject-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103820"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>NtGdiDdQueryDirectDrawObject-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Fragt eine zuvor erstellte Kernelmodusdarstellung eines Microsoft DirectDraw-Objekts nach seinen Funktionen ab.

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

*hDirectDrawLocal* \[ In\]
</dt> <dd>

Handle für das zuvor erstellte DirectDraw-Gerät im Kernelmodus.

</dd> <dt>

*pHalInfo* \[ out\]
</dt> <dd>

Zeiger auf eine [**\_ DD-INFO-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) die mit den Funktionen des Geräts gefüllt wird. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Zeiger auf einen vom Aufrufer bereitgestellten Puffer, der vom Treiber gemeldete Rückrufflags speichert. Der Puffer sollte die Größe 3 sizeof(DWORD) haben und Rückrufflags in der folgenden Reihenfolge \* speichern: pCallBackFlags 0 für \[ \] Flags in [**DD \_ CALLBACKS,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks)pCallBackFlags 1 für \[ \] Flags in [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)und pCallBackFlags 2 für \[ \] Flags in [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puD3dCallbacks* \[ out\]
</dt> <dd>

Zeiger auf eine Tabelle mit Direct3D-Rückrufzeigern. Die Tabelle wird mit Zeigern auf Funktionen in der Gdi32.dll, die einen Direct3D-Anzeigetreiber initieren. Diese Rückruftabelle ist identisch mit der D3DHAL \_ D3DCALLBACKS-Struktur, die in der DDK-Dokumentation erläutert wird.

</dd> <dt>

*puD3dDriverData* \[ out\]
</dt> <dd>

Zeiger auf [**D3DHAL \_ GLOBALDRIVERDATA-Daten,**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) wie in der DDK-Dokumentation beschrieben.

</dd> <dt>

*puD3dBufferCallbacks* \[ out\]
</dt> <dd>

Zeiger auf eine Tabelle mit Rückrufzeigern. Die Tabelle wird mit Zeigern auf Funktionen in der Gdi32.dll, die einen Direct3D-Anzeigetreiber initieren. Diese Rückruftabelle ist identisch mit der DDHAL \_ DDEXEBUFCALLBACKS-Struktur, die der [**DD \_ D3DBUFCALLBACKS-Struktur**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) entspricht, die in der DDK-Dokumentation erläutert wird, mit der Ausnahme, dass die Elemente XxxD3DBuffer in **\_ DD D3DBUFCALLBACKS** in DDHAL DDEXEBUFCALLBACKS durch XxxExecuteBuffer ersetzt \_ werden.

</dd> <dt>

*puD3dTextureFormats* \[ out\]
</dt> <dd>

Zeiger auf ein Array von [**DDSURFACEDESC-Strukturen,**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) die den Satz zulässiger Texturformate definieren.

</dd> <dt>

*puNumHeaps* \[ out\]
</dt> <dd>

Zeiger auf den **dwNumHeaps-Member** von [**\_ DDINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**. Der **dwNumHeaps-Member** gibt die Anzahl der Speicherheaps in *puvmList an.* Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puvmList* \[ out\]
</dt> <dd>

Zeiger auf eine Liste von Heapdeskriptoren für den Videospeicher. Kann NULL **sein.** Dieser Parameter wird nicht verwendet, da die Verwaltung des Videospeichers vollständig im Kernelmodus erfolgt.

</dd> <dt>

*puNumFourCC* \[ out\]
</dt> <dd>

Zeiger auf den **puNumFourCCCodes-Member** von [**DD \_ CODINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. Das **puNumFourCCCodes-Element** gibt die Anzahl von [FOURCC-Codes (Four-Character Codes)](../directshow/fourcc-codes.md) an, die der Treiber unterstützt. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*puFourCC* \[ out\]
</dt> <dd>

Zeiger auf eine Liste unterstützter [FOURCC-Oberflächenformate (Four-Character Codes).](../directshow/fourcc-codes.md) Kann NULL **sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dies erfolgreich ist, gibt diese Funktion **TRUE zurück.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Ein Aufruf dieser Funktion ist so konzipiert, dass er in einem zweistufigen Prozess erfolgt. Im ersten Schritt sollten *puFourCC,* *puvmList* und *puD3dTextureFormats* **NULL** sein, und [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) füllt [**\_ DDRATESINFO aus.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**ddCaps**. **dwNumFourCCCodes**, **\_ DDRATESINFO**.**vmiData**. **dwNumHeaps** und [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** mit der Anzahl von Einträgen, die zurückgegeben werden sollen. Im zweiten Aufruf sollte der Aufrufer Arrays der angegebenen Größe zuordnen und diese Zeiger anstelle von **NULL-Werten** in den *Parametern puFourCC,* *puvmList* und *puD3dTextureFormats* übergeben. Die Arrays werden dann mit den entsprechenden Daten aufgefüllt.

Anwendungen wird empfohlen, die DirectDraw- und [Direct3D-APIs zum](../direct3d10/d3d10-graphics-reference.md) Erstellen und Verwalten von Grafikgeräteobjekten zu verwenden. Diese Konstrukte abstrahieren den Prozess der Geräteerstellung auf vereinfachte und betriebssystemunabhängige Weise.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
