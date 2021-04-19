---
description: Definiert die Speicher Klasse, die die Puffer für eine Ressource enthält.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: D3DPOOL-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357244"
---
# <a name="d3dpool-enumeration"></a>D3DPOOL-Enumeration

Definiert die Speicher Klasse, die die Puffer für eine Ressource enthält.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ Standard**
</dt> <dd>

Ressourcen werden in den Speicherpool eingefügt, der sich am besten für den Satz von Verwendungen eignet, die für die jeweilige Ressource angefordert werden. Dabei handelt es sich in der Regel um Videospeicher, einschließlich des lokalen Video Speichers und des AGP-Speichers. Der D3DPOOL \_ -Standard Pool ist getrennt von D3DPOOL \_ Managed und D3DPOOL \_ SystemMem und gibt an, dass die Ressource für den Gerätezugriff im bevorzugten Speicher abgelegt wird. Beachten Sie, dass D3DPOOL \_ default niemals angibt, dass entweder D3DPOOL \_ Managed oder D3DPOOL \_ SystemMem als Speicher Pooltyp für diese Ressource ausgewählt werden soll. Texturen, die im D3DPOOL- \_ Standard Pool platziert werden, können nicht gesperrt werden, es sei denn, Sie sind dynamische Texturen oder private, FourCC-Treiber Formate. Um auf nicht Sperr Bare Texturen zuzugreifen, müssen Sie Funktionen wie [**IDirect3DDevice9:: updatesurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: getfrontbufferdata**](/windows/desktop/api)und [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api)verwenden. D3DPOOL \_ Managed ist für die meisten Anwendungen wahrscheinlich eine bessere Wahl als die D3DPOOL- \_ Standardeinstellung. Beachten Sie, dass einige Texturen, die in den vom Treiber proprietären Pixel Formaten erstellt wurden, für die Direct3D-Laufzeit unbekannt sind, gesperrt werden können. Beachten Sie auch, dass im Gegensatz zu Texturen-SwapChain-Back-Puffer, Renderziele, Scheitelpunkt Puffer und Index Puffer gesperrt werden können. Wenn ein Gerät verloren geht, müssen mit D3DPOOL default erstellte Ressourcen \_ freigegeben werden, [**bevor IDirect3DDevice9:: Reset**](/windows/desktop/api)aufgerufen wird. Weitere Informationen finden Sie unter [verlorene Geräte (Direct3D 9)](lost-devices.md).

Wenn beim Erstellen von Ressourcen mit der D3DPOOL- \_ Standardeinstellung für den Grafikkartenspeicher bereits ein Commit ausgeführt wurde, werden verwaltete Ressourcen entfernt, um genügend Arbeitsspeicher zum erfüllen der Anforderung freizugeben.

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ verwaltet**
</dt> <dd>

Ressourcen werden nach Bedarf automatisch in den Speicherzugriff auf das Gerät kopiert. Verwaltete Ressourcen werden durch den System Arbeitsspeicher unterstützt und müssen nicht neu erstellt werden, wenn ein Gerät verloren geht. Weitere Informationen finden Sie unter [Verwalten von Ressourcen (Direct3D 9)](managing-resources.md) . Verwaltete Ressourcen können gesperrt werden. Es wird nur die Systemspeicher Kopie direkt geändert. Direct3D kopiert die Änderungen nach Bedarf in den vom Treiber zugänglichen Arbeitsspeicher.



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DPOOL \_ Managed ist mit [**IDirect3DDevice9**](/windows/desktop/api)gültig, jedoch nicht mit [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SystemMem**
</dt> <dd>

Ressourcen werden in den Arbeitsspeicher eingefügt, der in der Regel nicht vom Direct3D-Gerät zugänglich ist. Diese Speicher Belegung beansprucht System-RAM, verringert jedoch nicht das kostenpflichtige RAM. Diese Ressourcen müssen nicht neu erstellt werden, wenn ein Gerät verloren geht. Die Ressourcen in diesem Pool können gesperrt werden und können als Quelle für einen [**IDirect3DDevice9:: updatesurface**](/windows/desktop/api) -oder [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) -Vorgang zu einer Speicher Ressource verwendet werden, die mit D3DPOOL default erstellt wurde \_ .

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ Scratch**
</dt> <dd>

Ressourcen werden im System-RAM abgelegt und müssen nicht neu erstellt werden, wenn ein Gerät verloren geht. Diese Ressourcen werden nicht durch die Größe von Geräten oder Formatierungs Beschränkungen gebunden. Aus diesem Grund kann auf diese Ressourcen nicht durch das Direct3D-Gerät zugegriffen werden, und es wird nicht als Texturen oder Renderziele festgelegt. Diese Ressourcen können jedoch immer erstellt, gesperrt und kopiert werden.

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle pooltypen sind mit allen Ressourcen gültig, einschließlich Scheitelpunkt Puffer, Index Puffer, Texturen und Oberflächen.

In den folgenden Tabellen werden die Einschränkungen für die pooltypen für Renderziele, tiefen Schablonen und dynamische und MipMap-Verwendungen angegeben. Ein x gibt eine kompatible Kombination an. das Fehlen von x deutet auf Inkompatibilität hin.



| Pool               | D3DUSAGE \_ renderTarget | D3DUSAGE \_ depthstencil |
|--------------------|------------------------|------------------------|
| D3DPOOL \_ Standard   | x                      | x                      |
| D3DPOOL \_ verwaltet   |                        |                        |
| D3DPOOL \_ Scratch   |                        |                        |
| D3DPOOL \_ SystemMem |                        |                        |



 



| Pool               | D3DUSAGE \_ dynamisch | D3DUSAGE \_ autogenmipmap |
|--------------------|-------------------|-------------------------|
| D3DPOOL \_ Standard   | x                 | x                       |
| D3DPOOL \_ verwaltet   |                   | x                       |
| D3DPOOL \_ Scratch   |                   |                         |
| D3DPOOL \_ SystemMem | x                 |                         |



 

Weitere Informationen zu Verwendungs Typen finden Sie unter [**D3DUSAGE**](d3dusage.md).

Pools können nicht für verschiedene Objekte gemischt werden, die in einer Ressource (MIP-Ebenen in einer MipMap) enthalten sind, und wenn ein Pool ausgewählt wird, kann er nicht geändert werden.

Anwendungen sollten D3DPOOL \_ für die meisten statischen Ressourcen verwenden, da dadurch die Anwendung nicht mehr mit verlorenen Geräten verarbeitet werden muss. (Verwaltete Ressourcen werden von der Laufzeit wieder hergestellt.) Dies ist besonders für die Systeme mit einheitlicher Speicherarchitektur (Unified Memory Architecture, Uma) vorteilhaft. Andere dynamische Ressourcen sind für D3DPOOL nicht gut geeignet \_ . Tatsächlich können Index Puffer und Vertex-Puffer nicht mit D3DPOOL erstellt werden, die \_ mit D3DUSAGE \_ Dynamic verwaltet werden.

Bei dynamischen Texturen ist es manchmal wünschenswert, ein paar von Grafikspeicher-und Systemspeicher Texturen zu verwenden und den Videospeicher mithilfe von D3DPOOL \_ default und dem Systemspeicher mithilfe von D3DPOOL \_ SystemMem zuzuordnen. Sie können die Bits der Systemspeicher Textur mithilfe einer Sperr Methode sperren und ändern. Anschließend können Sie die Grafikspeicher Textur mithilfe von [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)aktualisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DUSAGE**](d3dusage.md)
</dt> <dt>

[**IDirect3DDevice9:: kreatecubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[**IDirect3DDevice9:: kreateingedexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[**IDirect3DDevice9:: kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[**IDirect3DDevice9:: kreatevolumetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[**IDirect3DDevice9:: kreatevertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[**D3DINDEXBUFFER- \_ Abteilung**](d3dindexbuffer-desc.md)
</dt> <dt>

[**D3DSURFACE- \_ Abteilung**](d3dsurface-desc.md)
</dt> <dt>

[**D3DVERTEXBUFFER- \_ Abteilung**](d3dvertexbuffer-desc.md)
</dt> <dt>

[**D3DVOLUME- \_ Abteilung**](d3dvolume-desc.md)
</dt> </dl>

 

 
