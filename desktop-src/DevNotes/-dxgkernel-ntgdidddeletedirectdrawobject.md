---
description: Zerstört ein zuvor erstelltes Microsoft DirectDraw-Geräteobjekt im Kernelmodus.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: NtGdiDdDeleteDirectDrawObject-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 866624e35c5c05afa14692a2e83d1c15293af9435aa68deddf9c602b80820708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956549"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>NtGdiDdDeleteDirectDrawObject-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Zerstört ein zuvor erstelltes Microsoft DirectDraw-Geräteobjekt im Kernelmodus.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDrawLocal* 
</dt> <dd>

Handle für das DirectDraw-Geräteobjekt im Kernelmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dies erfolgreich ist, gibt diese Funktion **TRUE zurück.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Anwendungen wird empfohlen, die DirectDraw- und [Direct3D-APIs zum](../direct3d10/d3d10-graphics-reference.md) Erstellen und Verwalten von Grafikgeräteobjekten zu verwenden. Diese Konstrukte abstrahieren den Prozess der Geräteerstellung auf vereinfachte und betriebssystemunabhängige Weise.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**DdDeleteDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
