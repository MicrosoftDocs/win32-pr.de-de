---
title: ID3DX11DataProcessor-Schnittstelle (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Datenverarbeitungsobjekt, das von der ID3DX11ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- ID3DX11DataProcessor-Schnittstelle Direct3D 11
- ID3DX11DataProcessor-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 808c7d1bf1bdef1223e5b57e40ea5e6a90878101
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469347"
---
# <a name="id3dx11dataprocessor-interface"></a>ID3DX11DataProcessor-Schnittstelle

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Datenverarbeitungsobjekt, das von [**der ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md) zum asynchronen Laden von Daten verwendet wird.

## <a name="members"></a>Member

Die **ID3DX11DataProcessor-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataProcessor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11DataProcessor-Schnittstelle** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Erstellt ein Geräteobjekt.<br /> | 
| <a href="id3dx11dataprocessor-destroy.md"><strong>Zerstören</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Zerstört den Prozessor, nachdem ein Arbeitselement abgeschlossen wurde.<br /> | 
| <a href="id3dx11dataprocessor-process.md"><strong>Prozess</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Verarbeitet Daten.<br /> | 




 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann geerbt und seine Member für die Verarbeitung benutzerdefinierter Dateiformate neu definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

