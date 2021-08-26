---
title: ID3DX11ThreadPump-Schnittstelle (D3DX11core.h)
description: Ein Threadpump führt Aufgaben asynchron aus.
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
ms.openlocfilehash: f06f50e489503d02a6ea772be65678022dd36f6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481286"
---
# <a name="id3dx11threadpump-interface"></a>ID3DX11ThreadPump-Schnittstelle

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Ein Threadpump führt Aufgaben asynchron aus. Sie wird durch Aufrufen von [**D3DX11CreateThreadPump erstellt.**](d3dx11createthreadpump.md) Es gibt mehrere APIs, die eine optionale Threadpump als Parameter verwenden, z. B. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile;**](d3dx11compilefromfile.md) Wenn Sie eine Threadpumpschnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt. Insbesondere auf Multiprozessorcomputern kann eine Threadpump Ressourcen laden und Daten verarbeiten, ohne die Leistung merklich zu beeinträchtigen.

## <a name="members"></a>Member

Die **ID3DX11ThreadPump-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11ThreadPump** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11ThreadPump-Schnittstelle** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Fügt der Threadpump ein Arbeitselement hinzu.<br /> | 
| <a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Threadpump ab.<br /> | 
| <a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Ruft die Anzahl der Arbeitselemente in der Threadpump ab.<br /> | 
| <a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Legt Arbeitselemente auf dem Gerät fest, nachdem sie das Laden und Verarbeiten abgeschlossen haben.<br /> | 
| <a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Entfernt alle Arbeitselemente aus der Threadpump.<br /> | 
| <a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Wartet, bis alle Arbeitselemente in der Threadpump abgeschlossen sind.<br /> | 




 

## <a name="remarks"></a>Hinweise

### <a name="using-a-thread-pump"></a>Verwenden einer Threadpump

Die Threadpump lädt und verarbeitet Daten mithilfe des folgenden dreistufigen Prozesses:

1.  Laden und dekomprimieren Sie die Daten mit einem [**Datenlader.**](id3dx11dataloader.md) Das Datenladeobjekt verfügt über drei Methoden, die die Threadpump intern aufruft, während sie die Daten lädt und dekomprimiert: [**ID3DX11DataLoader::Load,**](id3dx11dataloader-load.md) [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)und [**ID3DX11DataLoader::D estster**](id3dx11dataloader-destroy.md). Die spezifische Funktionalität dieser drei APIs unterscheidet sich je nach Typ der daten, die geladen und dekomprimiert werden. Die Datenladeschnittstelle kann auch geerbt werden, und ihre APIs können geändert werden, wenn eine Datendatei geladen wird, die in einem eigenen benutzerdefinierten Format definiert ist.
2.  Verarbeiten Sie die Daten mit einem [**Datenprozessor.**](id3dx11dataprocessor.md) Das Datenprozessorobjekt verfügt über drei Methoden, die die Threadpump intern aufruft, während die Daten verarbeitet werden: [**ID3DX11DataProcessor::P rocess,**](id3dx11dataprocessor-process.md) [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)und [**ID3DX11DataProcessor::D estktor**](id3dx11dataprocessor-destroy.md). Die Art und Weise, wie die Daten verarbeitet werden, hängt vom Datentyp ab. Wenn es sich bei den Daten beispielsweise um eine Textur handelt, die als JPEG gespeichert ist, wird [**id3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) die JPEG-Dekomprimierung zum Erhalten der unformatierten Bildbits des Bilds verwenden. Wenn es sich bei den Daten um einen Shader handelt, kompiliert [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) die HLSL in bytecode. Nachdem die Daten verarbeitet wurden, wird ein Geräteobjekt für diese Daten erstellt (mit [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)), und das Objekt wird einer Warteschlange von Geräteobjekten hinzugefügt. Die Datenprozessorschnittstelle kann auch geerbt werden, und ihre APIs können geändert werden, wenn eine Datendatei verarbeitet wird, die in einem eigenen benutzerdefinierten Format definiert ist.
3.  Binden Sie das Geräteobjekt an das Gerät. Dies erfolgt, wenn die Anwendung [**ID3DX11ThreadPump::P rocessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md)aufruft, wodurch eine angegebene Anzahl von Objekten in der Warteschlange von Geräteobjekten an das Gerät gebunden wird.

Die Threadpump kann verwendet werden, um Daten auf zwei Arten zu laden: durch Aufrufen einer API, die eine Threadpump als Parameter akzeptiert, z. B. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile,**](d3dx11compilefromfile.md)oder durch Aufrufen von [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md). Im Fall der APIs, die einen Threadpump verwenden, werden das Datenlader und der Datenprozessor intern erstellt. Im Fall von AddWorkItem müssen das Datenlader und der Datenprozessor im Voraus erstellt und dann an AddWorkItem übergeben werden. D3DX11 stellt eine Reihe von APIs zum Erstellen von Datenladern und Datenprozessoren mit Funktionen zum Laden und Verarbeiten gängiger Datenformate zur Verfügung. Bei benutzerdefinierten Datenformaten müssen das Datenlader und die Datenprozessorschnittstellen geerbt und ihre Methoden neu definiert werden.

Das Threadpumpobjekt benötigt eine beträchtliche Menge an Ressourcen, sodass in der Regel nur eine pro Anwendung erstellt werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

