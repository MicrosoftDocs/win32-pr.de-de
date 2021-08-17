---
description: Beschreibt einen Indexpuffer.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC -Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7a25e56ccb9877fad6b370f9ed81c6c7dcf0744a96734b1e17d6dc3abbc0535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804933"
---
# <a name="d3dindexbuffer_desc-structure"></a>D3DINDEXBUFFER \_ DESC-Struktur

Beschreibt einen Indexpuffer.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das Oberflächenformat der Indexpufferdaten beschreibt.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**aufzählten D3DRESOURCETYPE-Typs,**](./d3dresourcetype.md) der diese Ressource als Indexpuffer identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kombination eines oder mehrerer der folgenden Flags, die die Verwendung für diese Ressource angeben.



| Wert                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Legen Sie fest, um anzugeben, dass für den Indexpufferinhalt nie clipping erforderlich ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ DYNAMIC**</dt> </dl>                                  | Legen Sie fest, um anzugeben, dass der Indexpuffer eine dynamische Speichernutzung erfordert. Dies ist für Treiber nützlich, da sie so entscheiden können, wo der Puffer gespeichert werden soll. Im Allgemeinen werden statische Indexpuffer im Videospeicher und dynamische Indexpuffer im AGP-Speicher platziert. Beachten Sie, dass es keine separate statische Verwendung gibt. Wenn Sie D3DUSAGE DYNAMIC nicht \_ angeben, wird der Indexpuffer als statisch festgelegt. D3DUSAGE DYNAMIC wird streng durch die \_ D3DLOCK DISCARD- und \_ D3DLOCK \_ NOOVERWRITE-Sperrflags erzwungen. Daher sind D3DLOCK DISCARD und D3DLOCK NOOVERWRITE nur für Indexpuffer gültig, die mit \_ \_ D3DUSAGE DYNAMIC erstellt wurden. Sie sind keine gültigen Flags für statische Scheitelpunktpuffer. \_<br/> Weitere Informationen zur Verwendung dynamischer Indexpuffer finden Sie unter [Verwenden von dynamischen Vertex- und Indexpuffern.](performance-optimizations.md)<br/> Beachten Sie, dass D3DUSAGE \_ DYNAMIC nicht für verwaltete Indexpuffer angegeben werden kann. Weitere Informationen finden Sie unter [Verwalten von Ressourcen (Direct3D 9).](managing-resources.md)<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Wird festgelegt, um anzugeben, wann der Indexpuffer zum Zeichnen von primitiven Hochordnungstypen verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**\_D3DUSAGE-NPATCHES**</dt> </dl>                               | Wird festgelegt, um anzugeben, wann der Indexpuffer zum Zeichnen von N Patches verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**D3DUSAGE \_ POINTS**</dt> </dl>                                     | Wird festgelegt, um anzugeben, wann der Indexpuffer zum Zeichnen von Punkt-Sprites oder indizierten Punktlisten verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Wird festgelegt, um anzugeben, dass der Puffer für die Softwareverarbeitung verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | Informiert das System, dass die Anwendung nur in den Indexpuffer schreibt. Mit diesem Flag kann der Treiber den besten Speicherort für effiziente Schreibvorgänge und Rendering auswählen. Versuche, aus einem Indexpuffer zu lesen, der mit dieser Funktion erstellt wird, können zu leistungsschädigenden Leistungssteigerungen führen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**enumerierten D3DPOOL-Typs,**](./d3dpool.md) der die Für diesen Indexpuffer zugeordnete Speicherklasse an gibt.

</dd> <dt>

**Größe**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des Indexpuffers in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Indexpuffer (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
