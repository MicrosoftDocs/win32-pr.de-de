---
title: ID3DX11DataLoader-Schnittstelle (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Datenladeobjekt, das von der ID3DX11ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- ID3DX11DataLoader-Schnittstelle Direct3D 11
- ID3DX11DataLoader-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b688fcbeff21edf23f6a3be1b39be5a9cf0000
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471646"
---
# <a name="id3dx11dataloader-interface"></a>ID3DX11DataLoader-Schnittstelle

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Datenladeobjekt, das von [**der ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md) zum asynchronen Laden von Daten verwendet wird.

## <a name="members"></a>Member

Die **ID3DX11DataLoader-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataLoader** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11DataLoader-Schnittstelle** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="id3dx11dataloader-decompress.md"><strong>Dekomprimieren</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Dekomprimiert codierte Daten.<br /> | 
| <a href="id3dx11dataloader-destroy.md"><strong>Zerstören</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Zerstört das Ladeprogramm, nachdem ein Arbeitselement abgeschlossen wurde.<br /> | 
| <a href="id3dx11dataloader-load.md"><strong>Laden</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Lädt Daten von einem Datenträger.<br /> | 




 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann geerbt und seine Member neu definiert werden. Auf diese Weise können Sie die API zum Laden und Dekomprimieren Ihrer eigenen benutzerdefinierten Dateiformate anpassen.

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

 

