---
title: ID3DX11ThreadPump-Schnittstelle (D3DX11core. h)
description: Ein Thread-Pump führt Aufgaben asynchron aus.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- ID3DX11ThreadPump-Schnittstelle Direct3D 11
- ID3DX11ThreadPump Interface Direct3D 11, beschrieben
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
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103070"
---
# <a name="id3dx11threadpump-interface"></a>ID3DX11ThreadPump-Schnittstelle

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Ein Thread-Pump führt Aufgaben asynchron aus. Sie wird durch Aufrufen von [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md)erstellt. Es gibt mehrere APIs, die ein optionales threadpump als Parameter akzeptieren, z. b. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile**](d3dx11compilefromfile.md). Wenn Sie eine Thread-Pump-Schnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt. Vor allem bei Multiprozessorcomputern kann ein Thread-Pump Ressourcen laden und Daten verarbeiten, ohne eine spürbare Leistungsminderung zu erzielen.

## <a name="members"></a>Member

Die **ID3DX11ThreadPump** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX11ThreadPump** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11ThreadPump** -Schnittstelle verfügt über diese Methoden.



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
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>Addworkitem</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Fügt der Thread Pumpe ein Arbeits Element hinzu.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>Getqueuestatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>Getworkitemcount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Ruft die Anzahl der Arbeitselemente in der Thread Pumpe ab.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>Processdeviceworkitems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Legt Arbeitselemente auf das Gerät fest, nachdem Sie geladen und verarbeitet wurden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>Purgeallitems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Löscht alle Arbeitselemente aus der Thread Pumpe.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>Waitforallitems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Wartet, bis alle Arbeitselemente in der Thread Pumpe abgeschlossen sind.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

### <a name="using-a-thread-pump"></a>Verwenden eines Thread Pump

Die Thread Pumpe lädt und verarbeitet Daten mit dem folgenden dreistufigen Prozess:

1.  Laden und decokomprimieren der Daten mit einem [**Daten Lader**](id3dx11dataloader.md). Das Data Loader-Objekt verfügt über drei Methoden, die vom threadpump intern beim Laden und Dekomprimieren der Daten aufgerufen werden: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D eComPress**](id3dx11dataloader-decompress.md)und [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md). Die spezifischen Funktionen dieser drei APIs unterscheiden sich abhängig vom Typ der geladenen und dekomprimierten Daten. Die Schnittstelle des Daten Laders kann auch geerbt werden, und die zugehörigen APIs können geändert werden, wenn eine Datendatei geladen wird, die in einem eigenen benutzerdefinierten Format definiert ist.
2.  Verarbeiten Sie die Daten mit einem [**Datenprozessor**](id3dx11dataprocessor.md). Das Data Processor-Objekt verfügt über drei Methoden, die von der Thread Pumpe intern aufgerufen werden, während Sie die Daten verarbeitet: [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: foratedeviceobject**](id3dx11dataprocessor-createdeviceobject.md)und [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md). Die Art und Weise, wie die Daten verarbeitet werden, unterscheidet sich je nach Art der Daten. Wenn es sich bei den Daten z. b. um eine Textur handelt, die als JPEG gespeichert ist, führt [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) eine JPEG-Komprimierung durch, um die rohbildbits des Bilds abzurufen. Wenn es sich bei den Daten um einen Shader handelt, kompiliert [**ID3DX11DataProcessor::P rocess**](id3dx11dataprocessor-process.md) den HLSL in Bytecode. Nachdem die Daten verarbeitet wurden, wird ein Geräte Objekt für diese Daten erstellt (mit [**ID3DX11DataProcessor:: kreatedeviceobject**](id3dx11dataprocessor-createdeviceobject.md)), und das Objekt wird einer Warteschlange von Geräte Objekten hinzugefügt. Die Datenprozessor Schnittstelle kann auch geerbt werden, und die zugehörigen APIs können geändert werden, wenn eine Datendatei verarbeitet wird, die in einem eigenen benutzerdefinierten Format definiert ist.
3.  Binden Sie das Geräte Objekt an das Gerät. Dies geschieht, wenn eine Anwendung [**ID3DX11ThreadPump::P rocess deviceworkitems**](id3dx11threadpump-processdeviceworkitems.md)aufruft, die eine angegebene Anzahl von Objekten in der Warteschlange von Geräte Objekten an das Gerät bindet.

Die Thread Pumpe kann zum Laden von Daten auf zwei Arten verwendet werden: durch Aufrufen einer API, die eine Thread Pumpe als Parameter annimmt, z. b. [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) und [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), oder durch Aufrufen von [**ID3DX11ThreadPump:: addworkitem**](id3dx11threadpump-addworkitem.md). Bei den APIs, die eine Thread Pumpe verwenden, werden der Daten Lader und der Datenprozessor intern erstellt. Im Fall von addworkitem müssen der Daten Lader und der Datenprozessor vorab erstellt und dann an addworkitem übergeben werden. Bibliothek d3dx11 bietet eine Reihe von APIs zum Erstellen von Daten Lade Programmen und Datenprozessoren mit Funktionen zum Laden und Verarbeiten von allgemeinen Datenformaten. Bei benutzerdefinierten Datenformaten müssen die Daten Lader-und Datenprozessor Schnittstellen geerbt werden, und ihre Methoden müssen neu definiert werden.

Das Thread-Pump Objekt nimmt eine beträchtliche Menge an Ressourcen in Rechnung, daher sollte im Allgemeinen nur eine pro Anwendung erstellt werden.

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

 

