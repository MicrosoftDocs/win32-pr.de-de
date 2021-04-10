---
description: Datenlade Objekt, das von der ID3DX10ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: ID3DX10DataLoader-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961616"
---
# <a name="id3dx10dataloader-interface"></a>ID3DX10DataLoader-Schnittstelle

Datenlade Objekt, das von der [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen Laden von Daten verwendet wird

## <a name="members"></a>Member

Die **ID3DX10DataLoader** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10DataLoader** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10DataLoader** -Schnittstelle verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dekomprimieren**](id3dx10dataloader-decompress.md) | Wird verwendet, um codierte Daten zu decodieren. Dies wird in der Regel zum Laden von Ressourcen aus Dateisystemen wie ZIP-Dateien verwendet. Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.<br/> |
| [**Zerstören**](id3dx10dataloader-destroy.md)       | Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um das Lade Modul zu zerstören, nachdem ein Arbeits Element abgeschlossen wurde<br/>                                                                                                   |
| [**Laden**](id3dx10dataloader-load.md)             | Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum Laden von Daten von einem Datenträger verwendet.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann geerbt und seine Member neu definiert werden. Auf diese Weise können Sie die API zum Laden und Dekomprimieren ihrer eigenen benutzerdefinierten Dateiformate anpassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
