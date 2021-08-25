---
title: ID3DX11ThreadPump-Schnittstelle (D3DX11core.h)
description: Eine Threadpumpe führt Aufgaben asynchron aus.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- ID3DX11ThreadPump-Schnittstelle Direct3D 11
- ID3DX11ThreadPump-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4bcfbc5fcf128f3ef71250180b487c83ce3c0d5430a563dfa3b7069e4235e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858040"
---
# <a name="id3dx11threadpump-interface"></a>ID3DX11ThreadPump-Schnittstelle

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

Eine Threadpumpe führt Aufgaben asynchron aus. Sie wird durch Aufrufen von [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md)erstellt. Es gibt mehrere APIs, die eine optionale Threadpumpe als Parameter verwenden, z. B. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Wenn Sie eine Threadpumpschnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt. Insbesondere auf Multiprozessorcomputern kann eine Threadpumpe Ressourcen laden und Daten verarbeiten, ohne dass die Leistung merklich abnimmt.

## <a name="members"></a>Member

Die **ID3DX11ThreadPump-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11ThreadPump** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11ThreadPump-Schnittstelle** verfügt über diese Methoden.



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
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.
</blockquote>
<br/> Fügt der Threadpumpe ein Arbeitselement hinzu.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.
</blockquote>
<br/> Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Threadpumpe ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.
</blockquote>
<br/> Ruft die Anzahl der Arbeitselemente in der Threadpumpe ab.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.
</blockquote>
<br/> Legt Arbeitselemente auf dem Gerät fest, nachdem sie geladen und verarbeitet wurden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.
</blockquote>
<br/> Löscht alle Arbeitselemente aus der Threadpumpe.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.
</blockquote>
<br/> Wartet, bis alle Arbeitselemente in der Threadpumpe abgeschlossen sind.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

### <a name="using-a-thread-pump"></a>Verwenden einer Threadpumpe

Die Threadpumpe lädt und verarbeitet Daten mithilfe des folgenden dreistufigen Prozesses:

1.  Laden und Dekomprimen der Daten mit einem [**Datenladeprogramm.**](id3dx11dataloader.md) Das Datenladeprogrammobjekt verfügt über drei Methoden, die die Threadpump beim Laden und Dekomprimieren der Daten intern aufruft: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)und [**ID3DX11DataLoader::D estobald**](id3dx11dataloader-destroy.md). Die spezifischen Funktionen dieser drei APIs unterscheiden sich je nach Typ der geladenen und dekomprimierten Daten. Die Datenladeprogrammschnittstelle kann auch geerbt werden, und ihre APIs können geändert werden, wenn eine Datendatei geladen wird, die im eigenen benutzerdefinierten Format definiert ist.
2.  Verarbeiten Sie die Daten mit einem [**Datenprozessor.**](id3dx11dataprocessor.md) Das Datenprozessorobjekt verfügt über drei Methoden, die die Threadpump intern aufruft, während es die Daten verarbeitet: [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)und [**ID3DX11DataProcessor::D est dll**](id3dx11dataprocessor-destroy.md). Die Art und Weise, wie die Daten verarbeitet werden, hängt vom Typ der Daten ab. Wenn es sich bei den Daten beispielsweise um eine als JPEG gespeicherte Textur handelt, führt [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) die JPEG-Dekomprimierung durch, um die unformatierten Bildbits des Bilds abzurufen. Wenn es sich bei den Daten um einen Shader handelt, kompiliert [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) die HLSL in Bytecode. Nachdem die Daten verarbeitet wurden, wird ein Geräteobjekt für diese Daten erstellt (mit [**ID3DX11DataProcessor::CreateDeviceObject),**](id3dx11dataprocessor-createdeviceobject.md)und das Objekt wird einer Warteschlange von Geräteobjekten hinzugefügt. Die Datenprozessorschnittstelle kann auch geerbt werden, und ihre APIs können geändert werden, wenn eine Datendatei im eigenen benutzerdefinierten Format definiert wird.
3.  Binden Sie das Geräteobjekt an das Gerät. Dies geschieht, wenn die Anwendung [**ID3DX11ThreadPump::P rocessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md)aufruft, wodurch eine angegebene Anzahl von Objekten in der Warteschlange von Geräteobjekten an das Gerät gebunden wird.

Die Threadpumpe kann zum Laden von Daten auf zwei Arten verwendet werden: durch Aufrufen einer API, die eine Threadpumpe als Parameter verwendet, z. B. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile,**](d3dx11compilefromfile.md)oder durch Aufrufen von [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md). Im Fall der APIs, die eine Threadpumpe verwenden, werden das Datenladeprogramm und der Datenprozessor intern erstellt. Im Fall von AddWorkItem müssen das Datenladeprogramm und der Datenprozessor vorab erstellt und dann an AddWorkItem übergeben werden. D3DX11 bietet eine Reihe von APIs zum Erstellen von Datenladern und Datenprozessoren, die funktionen zum Laden und Verarbeiten gängiger Datenformate aufweisen. Bei benutzerdefinierten Datenformaten müssen das Datenladeprogramm und die Datenprozessorschnittstellen geerbt und ihre Methoden neu definiert werden.

Das Threadpumpobjekt nimmt eine beträchtliche Menge an Ressourcen in Anspruch, sodass in der Regel nur eine pro Anwendung erstellt werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

