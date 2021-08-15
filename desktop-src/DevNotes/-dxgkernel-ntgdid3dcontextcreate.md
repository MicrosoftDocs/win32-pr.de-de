---
description: Erstellt einen Kontext.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: NtGdiD3DContextCreate-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: a11ae1d1e9b9469f22971ec3fc7447d8552b6d263bb43f4a8fe336ccbbc37a69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017738"
---
# <a name="ntgdid3dcontextcreate-function"></a>NtGdiD3DContextCreate-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Erstellt einen Kontext.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDrawLocal* \[ In\]
</dt> <dd>

Handle für ein DirectDraw-Objekt im Kernelmodus, das zuvor mit [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)erstellt wurde und das Gerät darstellt, auf dem der Direct3D-Kontext erstellt werden soll.

</dd> <dt>

*hColor* \[ In\]
</dt> <dd>

Handle für eine [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die DirectDraw-Oberfläche beschreibt, die als Renderingziel verwendet werden soll.

</dd> <dt>

*hUlaZ* \[ In\]
</dt> <dd>

Handle für eine [**DD \_ SURFACE \_ LOCAL-Struktur,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) die die DirectDraw-Oberfläche beschreibt, die als Tiefenpuffer verwendet werden soll. Wenn dieser Member **NULL** ist, muss keine Tiefenpufferung ausgeführt werden.

</dd> <dt>

*pdcci* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**D3DNTHAL \_ CONTEXTCREATEDATA-Struktur,**](/windows-hardware/drivers/ddi/) die die zum Erstellen eines Kontexts erforderlichen Informationen und die Daten enthält, die der Treiber im neuen Kontext speichern soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiD3DContextCreate** gibt einen der folgenden Rückrufcodes zurück.



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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
