---
description: Beschreibt einen Index Puffer.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961632"
---
# <a name="d3dindexbuffer_desc-structure"></a>D3DINDEXBUFFER- \_ Struktur

Beschreibt einen Index Puffer.

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

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format der Index Puffer Daten beschreibt.

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Index Puffer identifiziert.

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kombination aus einem oder mehreren der folgenden Flags, die die Verwendung für diese Ressource angeben.



| Wert                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DoNotClip**</dt> </dl>                            | Legen Sie fest, um anzugeben, dass der Inhalt des Index Puffers nie abgeschnitten werden muss.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ dynamisch**</dt> </dl>                                  | Legen Sie fest, um anzugeben, dass der Index Puffer eine dynamische Arbeitsspeicher Verwendung erfordert. Dies ist für Treiber nützlich, da Sie dadurch entscheiden können, wo der Puffer platziert werden soll. Im Allgemeinen werden statische Index Puffer in den Videospeicher eingefügt, und dynamische Index Puffer werden im AGP-Speicher abgelegt. Beachten Sie, dass es keine separate statische Verwendung gibt. Wenn Sie D3DUSAGE Dynamic nicht angeben, \_ wird der Index Puffer statisch gemacht. D3DUSAGE \_ Dynamic wird streng durch die \_ Sperr Flags D3DLOCK verwerfen und D3DLOCK \_ noüberschreibung erzwungen. Daher \_ sind D3DLOCK DISCARD und D3DLOCK \_ noüberschreibung nur für Index Puffer gültig, die mit D3DUSAGE Dynamic erstellt wurden \_ . Sie sind keine gültigen Flags für statische Scheitelpunkt Puffer.<br/> Weitere Informationen zur Verwendung dynamischer Index Puffer finden Sie unter [Verwenden von dynamischen Scheitelpunkt-und Index Puffern](performance-optimizations.md).<br/> Beachten Sie, dass D3DUSAGE \_ Dynamic nicht für verwaltete Index Puffer angegeben werden kann. Weitere Informationen finden Sie unter [Verwalten von Ressourcen (Direct3D 9)](managing-resources.md).<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ rtpatches**</dt> </dl>                            | Legen Sie fest, um anzugeben, wann der Index Puffer zum Zeichnen von grundlegenden primitiven verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ npatches**</dt> </dl>                               | Legen Sie fest, um anzugeben, wann der Index Puffer zum Zeichnen von N-Patches verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**D3DUSAGE \_ Punkte**</dt> </dl>                                     | Legen Sie fest, um anzugeben, wann der Index Puffer für Zeichnungs Punkt Sprites oder indizierte Punkt Listen verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ softwareprocessing**</dt> </dl> | Legen Sie fest, um anzugeben, dass der Puffer mit der Software Verarbeitung verwendet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ schreiben**</dt> </dl>                            | Informiert das System, dass die Anwendung nur in den Index Puffer schreibt. Wenn Sie dieses Flag verwenden, kann der Treiber den optimalen Speicherort für effiziente Schreibvorgänge und Rendering auswählen. Versuche, aus einem Index Puffer zu lesen, der mit dieser Funktion erstellt wird, können zu Leistungseinbußen führen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für diesen Index Puffer zugeordnete Arbeitsspeicher Klasse angibt.

</dd> <dt>

**Größe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe des Index Puffers in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Index Puffer (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
