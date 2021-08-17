---
description: Funktionsprototyp, der von D3DXComputeIMTFromSignal verwendet wird, um ein benutzerdefiniertes Signal im u,v-Raum eines Eingabegitters zu beschreiben. Die Funktion wertet ein prozedurales Signal der Dimension uSignalDimension an der angegebenen u,v-Koordinate aus.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e4f6ffaa4c844e755d489aae52dd13b8390da1145734d50f5865bbe0e3cfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728507"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Funktionsprototyp, der von [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) verwendet wird, um ein benutzerdefiniertes Signal im u,v-Raum eines Eingabegitters zu beschreiben. Die Funktion wertet ein prozedurales Signal der Dimension uSignalDimension an der angegebenen u,v-Koordinate aus.

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

\[in uPrimitiveId: Der Index des Eingabedreiecks im Netz, für \] das das Signal berechnet werden soll.

\[in \] uSignalDimension: Die Anzahl der float-Elemente, die im Array von Signaldaten (pfSignalOut) gespeichert werden.

\[in \] pUserData: Der pUserData-Zeiger, der an [**D3DXComputeIMTFromSignal übergeben wurde.**](d3dxcomputeimtfromsignal.md)

\[out \] pfSignalOut: Ein Array von floats, das die Signaldaten enthält.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, um S \_ OK zurück zu geben.

## <a name="remarks"></a>Hinweise

Achten Sie darauf, die Windows [**Datentypen**](../winprog/windows-data-types.md) beim Deklarieren der Rückruffunktion anzugeben. Andernfalls können Stapelüberläufe auftreten.



| Anforderung               | Wert            |
|----------------|-------------|
| Header         | d3dx9mesh.h |
| Importbibliothek | d3dx9.lib   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
