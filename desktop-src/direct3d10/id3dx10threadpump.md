---
description: Wird verwendet, um Aufgaben asynchron auszuführen und mit D3DX10CreateThreadPump erstellt zu werden.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: ID3DX10ThreadPump-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9fe3f0ca5955963864ef18de5d86fe03083d3f3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132413"
---
# <a name="id3dx10threadpump-interface"></a>ID3DX10ThreadPump-Schnittstelle

Wird verwendet, um Aufgaben asynchron auszuführen und mit [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md)erstellt zu werden. Es gibt mehrere d3dx10-APIs, die optional eine Thread Pumpe als Parameter verwenden können, wie z. b. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (Weitere Informationen finden Sie unter "Hinweise".) Wenn die Thread Pumpe an diese APIs weitergeleitet wird, werden Sie asynchron in einem separaten Thread Pump Thread ausgeführt. Der Vorteil hierbei ist, dass es das Laden und Verarbeiten großer Datenmengen bewirken kann, ohne dass eine Benachrichtigung über die Leistung auf dem Bildschirm angezeigt wird.

## <a name="members"></a>Member

Die **ID3DX10ThreadPump** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10ThreadPump** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10ThreadPump** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addworkitem**](id3dx10threadpump-addworkitem.md)                       | Fügen Sie der Thread Pumpe ein Arbeits Element hinzu.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Getqueuestatus**](id3dx10threadpump-getqueuestatus.md)                 | Gibt die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe an.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**Getworkitemcount**](id3dx10threadpump-getworkitemcount.md)             | Gibt die Anzahl der Arbeitselemente an, die sich zurzeit in der Thread Pumpe befinden.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**Processdeviceworkitems**](id3dx10threadpump-processdeviceworkitems.md) | Legen Sie die Arbeitselemente auf das Gerät fest, nachdem das Laden und verarbeiten abgeschlossen ist. Wenn die Thread Pumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird Sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. an diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt. Dies ist hilfreich, um die Verarbeitungs Menge zu steuern, die für die Bindung von Ressourcen an das Gerät für jeden Frame aufgewendet wird. Siehe Bemerkungen.<br/> |
| [**Purgeallitems**](id3dx10threadpump-purgeallitems.md)                   | Löschen Sie alle Arbeitselemente aus der Thread Pumpe.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**Waitforallitems**](id3dx10threadpump-waitforallitems.md)               | Warten Sie, bis alle Arbeitselemente in der Thread Pumpe abgeschlossen sind.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die Thread Pumpe lädt und verarbeitet Daten in einem 3-stufigen Prozess. Dies geschieht:

1.  Laden und decokomprimieren der Daten mit einem Daten Lader. Das Data Loader-Objekt verfügt über drei Methoden, die vom threadpump intern beim Laden und Dekomprimieren der Daten aufgerufen werden: [**ID3DX10DataLoader:: Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D eComPress**](id3dx10dataloader-decompress.md)und [**ID3DX10DataLoader::D estroy**](id3dx10dataloader-destroy.md). Die spezifischen Funktionen dieser drei APIs unterscheiden sich abhängig vom Typ der geladenen und dekomprimierten Daten. Die Schnittstelle des Daten Laders kann auch geerbt werden, und die zugehörigen APIs können geändert werden, wenn eine Datendatei geladen wird, die in einem eigenen benutzerdefinierten Format definiert ist.
2.  Verarbeiten Sie die Daten mit einem Datenprozessor. Das Data Processor-Objekt verfügt über drei Methoden, die von der Thread Pumpe intern aufgerufen werden, während Sie die Daten verarbeitet: [**ID3DX10DataProcessor::P rocess**](id3dx10dataprocessor-process.md), [**ID3DX10DataProcessor:: foratedeviceobject**](id3dx10dataprocessor-createdeviceobject.md)und [**ID3DX10DataProcessor::D estroy**](id3dx10dataprocessor-destroy.md). Die Art und Weise, wie die Daten verarbeitet werden, unterscheidet sich je nach Art der Daten. Wenn es sich bei den Daten z. b. um eine Textur handelt, die als JPEG gespeichert ist, führt **ID3DX10DataProcessor::P rocess** eine JPEG-Komprimierung durch, um die rohbildbits des Bilds abzurufen. Wenn es sich bei den Daten um einen Shader handelt, kompiliert **ID3DX10DataProcessor::P rocess** den HLSL in Bytecode. Nachdem die Daten verarbeitet wurden, wird ein Geräte Objekt für diese Daten erstellt (mit **ID3DX10DataProcessor:: kreatedeviceobject**), und das Objekt wird einer Warteschlange von Geräte Objekten hinzugefügt. Die Datenprozessor Schnittstelle kann auch geerbt werden, und die zugehörigen APIs können geändert werden, wenn eine Datendatei verarbeitet wird, die in einem eigenen benutzerdefinierten Format definiert ist.
3.  Binden Sie das Geräte Objekt an das Gerät. Dies geschieht, wenn eine Anwendung [**ID3DX10ThreadPump::P rocess deviceworkitems**](id3dx10threadpump-processdeviceworkitems.md)aufruft, die eine angegebene Anzahl von Objekten in der Warteschlange von Geräte Objekten an das Gerät bindet.

Die Thread Pumpe kann zum Laden von Daten auf zwei Arten verwendet werden: durch Aufrufen einer API, die eine Thread Pumpe als Parameter annimmt, z. b. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und [**D3DX10CompileFromFile**](d3dx10compilefromfile.md), oder durch Aufrufen von [**ID3DX10ThreadPump:: addworkitem**](id3dx10threadpump-addworkitem.md). Bei den APIs, die eine Thread Pumpe verwenden, werden der Daten Lader und der Datenprozessor intern erstellt. Im Fall von **addworkitem** müssen der Daten Lader und der Datenprozessor vorab erstellt und dann an addworkitem übergeben werden. D3dx10 bietet eine Reihe von APIs zum Erstellen von Daten Lade Programmen und Datenprozessoren mit Funktionen zum Laden und Verarbeiten von allgemeinen Datenformaten (Weitere Informationen finden Sie in den Hinweisen zur kompletten Liste der APIs). Bei benutzerdefinierten Datenformaten müssen die Daten Lader-und Datenprozessor Schnittstellen geerbt werden, und ihre Methoden müssen neu definiert werden.

Das Thread-Pump Objekt nimmt eine beträchtliche Menge an Ressourcen in Rechnung, daher sollte im Allgemeinen nur eine pro Anwendung erstellt werden.

Integrierte d3dx10-Daten Lader



|                                                                            |                                          |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Erstellen Sie ein Datei Lade Modul asynchron.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Asynchrones Erstellen eines Daten Laders.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Erstellen Sie ein Ressourcen Lade Modul asynchron. |



 

Integrierte d3dx10-Datenprozessoren



|                                                                                                  |                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Erstellen Sie einen Datenprozessor, der mit einem threadpump verwendet werden soll. Diese API ähnelt D3DX10CreateAsyncTextureInfoProcessor, aber Sie lädt auch die Textur. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Erstellen Sie einen Datenprozessor, der mit einem threadpump verwendet werden soll.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Kompilieren Sie einen Shader, und erstellen Sie asynchron einen Datenprozessor.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Erstellen Sie asynchron einen Effekt mit einem Datenprozessor.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Erstellen Sie einen Effekt Pool asynchron.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Asynchrones Erstellen eines Daten Prozessors.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Erstellen Sie einen Datenprozessor für einen Shader asynchron.                                                                                               |



 

APIs, die eine Thread Pumpe als Parameter akzeptieren.



|                                                                                                  |                                                                  |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Kompilieren Sie einen Shader aus einer Datei.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Kompilieren Sie einen Shader, der sich im Speicher befindet.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Kompilieren Sie einen Shader aus einer Ressource.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Erstellen Sie einen Effekt aus einer Datei.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Erstellen Sie einen Effekt aus dem Arbeitsspeicher.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Erstellen Sie einen Effekt aus einer Ressource.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Erstellen Sie einen Effekt Pool aus einer Datei.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Erstellen Sie einen Effekt Pool aus einer Datei, die sich im Arbeitsspeicher befindet.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Erstellen Sie einen Effekt Pool aus einer Ressource.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Erstellen Sie einen Shader aus einer Datei, ohne ihn zu kompilieren.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei im Arbeitsspeicher.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Ressource.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Ruft Informationen zu einer angegebenen Bilddatei ab.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Sie erhalten Informationen zu einem bereits in den Arbeitsspeicher geladenen Image.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Ruft Informationen zu einem angegebenen Bild in einer Ressource ab.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Erstellen Sie eine Textur Ressource aus einer Datei.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Erstellen Sie eine Textur Ressource aus einer Datei, die sich im Systemspeicher befindet. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Erstellen Sie eine Textur Ressource aus einer anderen Ressource.                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
