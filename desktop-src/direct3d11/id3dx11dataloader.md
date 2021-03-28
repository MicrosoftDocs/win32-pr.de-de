---
title: ID3DX11DataLoader-Schnittstelle (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Datenlade Objekt, das von der ID3DX11ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- ID3DX11DataLoader-Schnittstelle Direct3D 11
- ID3DX11DataLoader Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: 68236451bf2ba6f491d17541f7d4ca627f5063c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103071"
---
# <a name="id3dx11dataloader-interface"></a>ID3DX11DataLoader-Schnittstelle

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Datenlade Objekt, das von der [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md) zum asynchronen Laden von Daten verwendet wird

## <a name="members"></a>Member

Die **ID3DX11DataLoader** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX11DataLoader** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11DataLoader** -Schnittstelle verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-decompress.md"><strong>Dekomprimieren</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Decodiert codierte Daten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataloader-destroy.md"><strong>Zerstören</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Zerstört das Lade Modul, nachdem ein Arbeits Element abgeschlossen wurde.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-load.md"><strong>Laden</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Lädt Daten von einem Datenträger.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann geerbt und seine Member neu definiert werden. Auf diese Weise können Sie die API zum Laden und Dekomprimieren ihrer eigenen benutzerdefinierten Dateiformate anpassen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

