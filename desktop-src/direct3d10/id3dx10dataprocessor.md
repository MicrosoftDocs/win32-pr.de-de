---
description: Datenverarbeitungsobjekt, das von der ID3DX10ThreadPump-Schnittstelle für die asynchrone Verarbeitung geladener Daten verwendet wird.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: ID3DX10DataProcessor-Schnittstelle (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ddb192a0591ce241e216b3bd0471212fc4801fbf1c901430c187f5370237049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128370"
---
# <a name="id3dx10dataprocessor-interface"></a>ID3DX10DataProcessor-Schnittstelle

Datenverarbeitungsobjekt, das von [**der ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) für die asynchrone Verarbeitung geladener Daten verwendet wird.

## <a name="members"></a>Member

Die **ID3DX10DataProcessor-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataProcessor** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10DataProcessor-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Erstellen Sie ein Geräteobjekt.<br/>                                                                                                  |
| [**Zerstören**](id3dx10dataprocessor-destroy.md)                       | Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um den Prozessor zu zerstören, nachdem ein Arbeitselement abgeschlossen wurde.<br/> |
| [**Prozess**](id3dx10dataprocessor-process.md)                       | Verarbeiten sie einige Daten.<br/>                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann geerbt und seine Member neu definiert werden. Auf diese Weise können Sie die API für die Verarbeitung Ihrer eigenen benutzerdefinierten Dateiformate anpassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
