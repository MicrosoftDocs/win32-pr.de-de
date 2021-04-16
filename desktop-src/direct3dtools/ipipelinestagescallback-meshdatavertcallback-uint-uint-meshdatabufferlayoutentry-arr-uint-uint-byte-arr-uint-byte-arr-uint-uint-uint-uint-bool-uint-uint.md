---
description: Ein Rückruf, der den Host der Pipeline Stufen Mesh-Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipipelinestagescallback:: meshdatavertcallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521387"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Ipipelinestagescallback:: meshdatavertcallback-Methode

Ein Rückruf, der den Host der Pipeline Stufen Mesh-Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>Parameter

*numvertices*   
Die Anzahl der Vertices in den Ergebnissen.

*numbufferlayoutentries*   
Die Anzahl der Puffer Layout-Einträge in den Ergebnissen.

*count1- \_ Einträge*   
Die Puffer Layout-entierung. Diese beschreiben die Shader-Ausgabe Signatur.

*Schritt*   
Die Größe (stride) eines gesamten Ausgabe Segments.

*numvbbytes*   
Die Größe des Scheitelpunkt Puffers in Bytes.

*count4 \_ pvbdata*   
Der Scheitelpunkt Puffer.

*numibbytes*   
Die Größe des Index Puffers in Bytes.

*count6 \_ pibdata*   
Der Index Puffer.

*indexSize*   
Die Größe der einzelnen Indizes in Bytes.

*Iboffset*   
Ein Offset im Index Puffer, der angibt, wo Indizes verwendet werden sollen.

*basevertex*   
Ein Offset in den Scheitelpunkt Puffer, der angibt, wo Scheitel Punkte verwendet werden sollen.

*minvertex*   

*Ibindexesvb*   
true, wenn der Index Puffer verwendet wird. andernfalls false.

*numindizes*   
Die Anzahl der verwendeten Indizes.

*Topologie*   
Die topolologie des Shaders. Dies ist nicht notwendigerweise identisch mit der Topologie des zugeordneten Draw-Aufrufes.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipipelinestagescallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
