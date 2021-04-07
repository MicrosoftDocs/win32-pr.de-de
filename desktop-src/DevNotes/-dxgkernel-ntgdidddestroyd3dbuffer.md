---
description: Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus, das mit dem dwcaps-Member der DDSCAPS-Struktur erstellt wurde, die auf DDSCAPS \_ executebuffer festgelegt ist.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: NtGdiDdDestroyD3DBuffer-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747720"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a>NtGdiDdDestroyD3DBuffer-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus, das mit dem **dwcaps** -Member der [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) -Struktur erstellt wurde, die auf DDSCAPS \_ executebuffer festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsurface* \[ in\]
</dt> <dd>

Handle für eine [**DD \_ destroysurfacedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) -Struktur, die die Informationen enthält, die zum Zerstören eines Direct3D-Befehls oder Scheitelpunkt Puffers erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdDestroyD3DBuffer** gibt einen der folgenden Rückruf Codes zurück.



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

 

 
