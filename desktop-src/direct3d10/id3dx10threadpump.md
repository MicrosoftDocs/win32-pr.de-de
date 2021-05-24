---
description: Wird zum asynchronen Ausführen von Aufgaben verwendet und mit D3DX10CreateThreadPump erstellt.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: ID3DX10ThreadPump-Schnittstelle (D3DX10.h)
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
ms.openlocfilehash: aecab39b655998533c80f1fff56e3f10d941f551
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335654"
---
# <a name="id3dx10threadpump-interface"></a>ID3DX10ThreadPump-Schnittstelle

Wird zum asynchronen Ausführen von Tasks verwendet und mit [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md)erstellt. Es gibt mehrere D3DX10-APIs, die optional eine Threadpumpe als Parameter verwenden können, z. B. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (eine vollständige Liste finden Sie in den Hinweisen). Wenn die Threadpumpe an diese APIs übergeben wird, werden sie asynchron auf einem separaten Threadpumpthread ausgeführt. Der Vorteil besteht darin, dass dadurch große Datenmengen geladen und verarbeitet werden können, ohne dass die Leistung auf dem Bildschirm erkennbar verlangsamt wird.

## <a name="members"></a>Member

Die **ID3DX10ThreadPump-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10ThreadPump** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10ThreadPump-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Fügen Sie der Threadpumpe ein Arbeitselement hinzu.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Abrufen der Anzahl von Elementen in jeder der drei Warteschlangen innerhalb der Threadpumpe.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Abrufen der Anzahl der Arbeitselemente, die sich derzeit in der Threadpumpe befinden.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | Legen Sie Arbeitselemente auf das Gerät fest, nachdem sie das Laden und Verarbeiten abgeschlossen haben. Wenn die Threadpumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. An diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt. Dies ist nützlich, um die Verarbeitungsmenge zu steuern, die für das Binden von Ressourcen an das Gerät für jeden Frame aufgewendet wird. Siehe Bemerkungen.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Löschen Sie alle Arbeitselemente aus der Threadpump.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Warten Sie, bis alle Arbeitselemente in der Threadpump abgeschlossen sind.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die Threadpump lädt und verarbeitet Daten in einem dreistufigen Prozess. Es geht um:

1.  Laden und dekomprimieren Sie die Daten mit einem Datenlader. Das Datenladeobjekt verfügt über drei Methoden, die die Threadpump intern aufruft, während sie die Daten lädt und dekomprimiert: [**ID3DX10DataLoader::Load,**](id3dx10dataloader-load.md) [**ID3DX10DataLoader::D ecompress**](id3dx10dataloader-decompress.md)und [**ID3DX10DataLoader::D estkennung.**](id3dx10dataloader-destroy.md) Die spezifische Funktionalität dieser drei APIs unterscheidet sich je nach Typ der daten, die geladen und dekomprimiert werden. Die Datenladeschnittstelle kann auch geerbt werden, und ihre APIs können geändert werden, wenn eine Datendatei geladen wird, die in einem eigenen benutzerdefinierten Format definiert ist.
2.  Verarbeiten Sie die Daten mit einem Datenprozessor. Das Datenprozessorobjekt verfügt über drei Methoden, die die Threadpump intern aufruft, während die Daten verarbeitet werden: [**ID3DX10DataProcessor::P rocess,**](id3dx10dataprocessor-process.md) [**ID3DX10DataProcessor::CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md)und [**ID3DX10DataProcessor::D estktor**](id3dx10dataprocessor-destroy.md). Die Art und Weise, wie die Daten verarbeitet werden, hängt vom Datentyp ab. Wenn es sich bei den Daten beispielsweise um eine Textur handelt, die als JPEG gespeichert ist, erfolgt die JPEG-Dekomprimierung durch **ID3DX10DataProcessor::P rocess,** um die unformatierten Bildbits des Bilds zu erhalten. Wenn es sich bei den Daten um einen Shader handelt, kompiliert **ID3DX10DataProcessor::P rocess** die HLSL in Bytecode. Nachdem die Daten verarbeitet wurden, wird ein Geräteobjekt für diese Daten erstellt (mit **ID3DX10DataProcessor::CreateDeviceObject**), und das Objekt wird einer Warteschlange von Geräteobjekten hinzugefügt. Die Datenprozessorschnittstelle kann auch geerbt werden, und ihre APIs können geändert werden, wenn eine Datendatei verarbeitet wird, die in einem eigenen benutzerdefinierten Format definiert ist.
3.  Binden Sie das Geräteobjekt an das Gerät. Dies geschieht, wenn die Anwendung [**ID3DX10ThreadPump::P rocessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md)aufruft, wodurch eine angegebene Anzahl von Objekten in der Warteschlange von Geräteobjekten an das Gerät gebunden wird.

Die Threadpumpe kann zum Laden von Daten auf zwei Arten verwendet werden: durch Aufrufen einer API, die eine Threadpumpe als Parameter verwendet, z. B. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und [**D3DX10CompileFromFile,**](d3dx10compilefromfile.md)oder durch Aufrufen von [**ID3DX10ThreadPump::AddWorkItem**](id3dx10threadpump-addworkitem.md). Im Fall der APIs, die eine Threadpumpe verwenden, werden das Datenladeprogramm und der Datenprozessor intern erstellt. Im Fall von **AddWorkItem** müssen das Datenladeprogramm und der Datenprozessor im Voraus erstellt und dann an AddWorkItem übergeben werden. D3DX10 bietet eine Reihe von APIs zum Erstellen von Datenladern und Datenprozessoren mit Funktionen zum Laden und Verarbeiten allgemeiner Datenformate (eine vollständige Liste der APIs finden Sie in den Hinweisen). Bei benutzerdefinierten Datenformaten müssen das Datenladeprogramm und die Datenprozessorschnittstellen geerbt und ihre Methoden neu definiert werden.

Das Threadpumpobjekt nimmt eine beträchtliche Menge an Ressourcen in Anspruch, sodass in der Regel nur eine pro Anwendung erstellt werden sollte.

Integrierte D3DX10-Datenlader



|                                                                           |  Beschreibung                                        |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Erstellen Sie asynchron ein Dateiladeprogramm.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Erstellen Sie asynchron ein Datenladeprogramm.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Erstellen Sie asynchron ein Ressourcenladeprogramm. |



 

Integrierte D3DX10-Datenprozessoren



|                                                                                                 |  Beschreibung                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Erstellen Sie einen Datenprozessor, der mit einer Threadpumpe verwendet werden soll. Diese API ähnelt D3DX10CreateAsyncTextureInfoProcessor, lädt aber auch die Textur. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Erstellen Sie einen Datenprozessor, der mit einer Threadpumpe verwendet werden soll.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Kompilieren Sie einen Shader, und erstellen Sie einen Datenprozessor asynchron.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Erstellen Sie asynchron einen Effekt mit einem Datenprozessor.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Erstellen Sie asynchron einen Effektpool.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Asynchrones Erstellen eines Datenprozessors.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Erstellen Sie asynchron einen Datenprozessor für einen Shader.                                                                                               |



 

APIs, die eine Threadpump als Parameter verwenden.



|                                                                                                 | Beschreibung                                                                 |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Kompilieren Sie einen Shader aus einer Datei.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Kompilieren Sie einen Shader im Arbeitsspeicher.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Kompilieren Sie einen Shader aus einer Ressource.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Erstellen Sie einen Effekt aus einer Datei.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Erstellen Sie einen Effekt aus dem Arbeitsspeicher.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Erstellen sie einen Effekt aus einer Ressource.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Erstellen Sie einen Effektpool aus einer Datei.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Erstellen Sie einen Effektpool aus einer Datei, die sich im Arbeitsspeicher befindet.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Erstellen sie einen Effektpool aus einer Ressource.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Erstellen Sie einen Shader aus einer Datei, ohne ihn zu kompilieren.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Erstellen Sie eine Shader-Ressourcenansicht aus einer Datei.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Erstellen Sie eine Shader-Ressourcenansicht aus einer Datei im Arbeitsspeicher.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Erstellen Sie eine Shader-Ressourcenansicht aus einer Ressource.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Ruft Informationen zu einer bestimmten Bilddatei ab.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Hier erfahren Sie, wie Sie Informationen zu einem bereits in den Arbeitsspeicher geladenen Image erhalten.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Erstellen Sie eine Texturressource aus einer Datei.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Erstellen Sie eine Texturressource aus einer Datei im Systemspeicher. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Erstellen Sie eine Texturressource aus einer anderen Ressource.                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
