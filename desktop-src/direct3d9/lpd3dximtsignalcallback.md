---
description: Funktionsprototyp, der von D3DXComputeIMTFromSignal verwendet wird, um ein benutzerdefiniertes Signal im u,v-Bereich eines Eingabegitters zu beschreiben. Die Funktion wertet ein prozedurales Signal der Dimension uSignalDimension an der bereitgestellten u,v-Koordinate aus.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342835"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Funktionsprototyp, der von [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) verwendet wird, um ein benutzerdefiniertes Signal im u,v-Bereich eines Eingabegitters zu beschreiben. Die Funktion wertet ein prozedurales Signal der Dimension uSignalDimension an der bereitgestellten u,v-Koordinate aus.

## <a name="syntax"></a>Syntax


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>Parameter

\[in \] uv: Ein Zeiger auf einen Vektor, der die Scheitelpunkttexturkoordinate enthält.

\[in \] uPrimitiveId: Der Index des Eingabedreiecks auf dem Gitternetz, für das das Signal berechnet werden soll.

\[in \] uSignalDimension: Die Anzahl der Gleitkommazahlen, die im Array von Signaldaten (pfSignalOut) gespeichert werden sollen.

\[in \] pUserData: Der an [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)übergebene pUserData-Zeiger.

\[out \] pfSignalOut: Ein Array von Gleitkommawerten, das die Signaldaten enthält.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, um S \_ OK zurückzugeben.

## <a name="remarks"></a>Hinweise

Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufrufkonvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben. Andernfalls können Stapelüberläufe auftreten.



| Anforderung               | Wert            |
|----------------|-------------|
| Header         | d3dx9mesh.h |
| Importbibliothek | d3dx9.lib   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
