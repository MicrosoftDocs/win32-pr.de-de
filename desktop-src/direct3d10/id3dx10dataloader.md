---
description: Datenladeobjekt, das von der ID3DX10ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: ID3DX10DataLoader-Schnittstelle (D3DX10.h)
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
ms.openlocfilehash: 86da40dd581c10d9f567f6011cd3987710a9aa36e41f360dc4ffc2662f909c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128358"
---
# <a name="id3dx10dataloader-interface"></a>ID3DX10DataLoader-Schnittstelle

Datenladeobjekt, das von [**der ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen Laden von Daten verwendet wird.

## <a name="members"></a>Member

Die **ID3DX10DataLoader-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataLoader** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10DataLoader-Schnittstelle** verfügt über diese Methoden.



| Methode                                             | Beschreibung                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dekomprimieren**](id3dx10dataloader-decompress.md) | Wird verwendet, um codierte Daten zu dekomprimiert. In der Regel wird dies verwendet, um Ressourcen aus Dateisystemen wie ZIP-Dateien zu laden. Beim Laden aus einer nicht komprimierten Ressource muss die Dekomprimierungsphase keine Arbeit leisten.<br/> |
| [**Zerstören**](id3dx10dataloader-destroy.md)       | Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um das Ladeprogramm nach Abschluss eines Arbeitselements zu zerstören.<br/>                                                                                                   |
| [**Laden**](id3dx10dataloader-load.md)             | Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um Daten von einem Datenträger zu laden.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann geerbt und seine Member neu definiert werden. Auf diese Weise können Sie die API zum Laden und Dekomprimieren Ihrer eigenen benutzerdefinierten Dateiformate anpassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
