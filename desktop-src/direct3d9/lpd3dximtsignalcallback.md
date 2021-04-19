---
description: Funktionsprototyp, der von D3DXComputeIMTFromSignal verwendet wird, um ein benutzerdefiniertes Signal im u-v-Raum eines Eingabe Netzes zu beschreiben. Die-Funktion wertet ein prozedurales Signal der Dimension usignaldimension bei der angegebenen u-, v-Koordinate aus.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343118"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Funktionsprototyp, der von [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) verwendet wird, um ein benutzerdefiniertes Signal im u-v-Raum eines Eingabe Netzes zu beschreiben. Die-Funktion wertet ein prozedurales Signal der Dimension usignaldimension bei der angegebenen u-, v-Koordinate aus.

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

\[in \] UV-ein Zeiger auf einen Vektor, der die Scheitelpunkt Textur Koordinate enthält.

\[in \] uprimitiveid: der Index des Eingabe Dreiecks in dem Mesh, für das das Signal berechnet werden soll.

\[in \] usignaldimension: die Anzahl von Gleit Komma Zahlen, die im Array von Signaldaten (pfsignalout) gespeichert werden sollen.

\[in \] puserdata: der puserdata-Zeiger, der an [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)weitergegeben wurde.

\[Out \] pfsignalout: ein Array von Gleit Komma Zahlen, das die Signaldaten enthält.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, damit S "OK" zurückgegeben wird \_ .

## <a name="remarks"></a>Bemerkungen

Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben. Andernfalls können Stapel Überläufe auftreten.



|                |             |
|----------------|-------------|
| Header         | d3dx9mesh. h |
| Importbibliothek | d3dx9. lib   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
