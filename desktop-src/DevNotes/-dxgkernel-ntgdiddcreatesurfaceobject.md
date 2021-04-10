---
description: Erstellt ein Surface-Objekt im Kernelmodus, das das Benutzermodus-Surface-Objekt darstellt, auf das von pusurfacelocal verwiesen wird.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Ntgdiddkreatesurfaceobject-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041351"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>Ntgdiddkreatesurfaceobject-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Erstellt ein Surface-Objekt im Kernelmodus, das das Benutzermodus-Surface-Objekt darstellt, auf das von *pusurfacelocal* verwiesen wird.

## <a name="syntax"></a>Syntax


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdrawlocal* \[ in\]
</dt> <dd>

Handle für den kernelmodusdirectdraw-Objekt.

</dd> <dt>

*hsurface* \[ in\]
</dt> <dd>

Vorheriges Handle für dieselbe Oberfläche. Wird verwendet, wenn die Oberfläche nach einem Modusschalter neu erstellt wird.

</dd> <dt>

*pusurfakelocal* \[ in\]
</dt> <dd>

Ein Zeiger auf [**die \_ \_ lokale DD-Oberflächen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) Struktur, die das DirectDraw-Benutzermodus-Surface-Objekt darstellt, dem der zugeordnete Arbeitsspeicher zugeordnet werden soll. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*pusurfakemore* \[ in\]
</dt> <dd>

Zeiger auf die [**DD- \_ Oberfläche \_ mehr**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) Struktur, die zusätzliche lokale Daten für jedes einzelne Surface-Objekt enthält. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*pusurfakeglobal* \[ in\]
</dt> <dd>

Zeiger zur [**\_ \_ globalen**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) TT-Oberflächenstruktur, die Oberflächendaten enthält, die Global mit mehreren Oberflächen gemeinsam genutzt werden. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*bcomplete* \[ in\]
</dt> <dd>

Kernel Modus-objektvervollständigungs Kennzeichen. Kann einen der folgenden Werte aufweisen.

<dt>



 Fall


</dt> <dd>

Vervollständigen Sie die gesamte Verarbeitung in Bezug auf die Kernel Modus-Darstellung.

</dd> <dt>



 Alarm


</dt> <dd>

Erstellen Sie das-Objekt, aber richten Sie keine internen Daten ein, z. b. den Speicher Zeiger. Mit **false** erstellte Objekte können mithilfe von [**ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md) angefügt und durch einen-Befehl von [**ntgdiddkreatesurface**](-dxgkernel-ntgdiddcreatesurface.md)abgeschlossen werden.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Funktion ein Handle für die Darstellung des kernelmodusausdrucks zurück. Andernfalls wird **null** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

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

[**Ddkreatesurfaceobject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**Ntgdidddelta etesurfaceobject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**Ntgdiddattachsurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**Ntgdiddkreatesurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
