---
description: Diese Tabelle ordnet Member einer D3DVERTEXELEMENT9-Deklaration einem FVF-Code zu.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Zuordnung zwischen einer Direct3D-Deklaration und einem f-Code (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124478"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Zuordnung zwischen einer Direct3D-Deklaration und einem f-Code (Direct3D 9)

Diese Tabelle ordnet Member einer [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Deklaration einem FVF-Code zu.



| Datentyp             | Verbrauch                      | Verwendungs Index | F-VF                       |
|-----------------------|----------------------------|-------------|---------------------------|
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE- \_ Position     | 0           | D3DFVF \_ XYZ               |
| D3DDECLTYPE \_ float4   | D3DDECLUSAGE \_ positiont    | 0           | D3DFVF \_ xyzrhw            |
| D3DDECLTYPE \_ floatn   | D3DDECLUSAGE \_ blendweight  | 0           | D3DFVF \_ xyzbn             |
| D3DDECLTYPE \_ UBYTE4   | D3DDECLUSAGE \_ blendindices | 0           | D3DFVF \_ xyzb (ngewichtungen + 1) |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ Normal       | 0           | D3DFVF \_ Normal            |
| D3DDECLTYPE \_ FLOAT1   | D3DDECLUSAGE \_ Psize        | 0           | D3DFVF \_ Psize             |
| D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE- \_ Farbe        | 0           | D3DFVF \_ diffuses           |
| D3DDECLTYPE \_ D3DCOLOR | D3DDECLUSAGE- \_ Farbe        | 1           | D3DFVF \_ Glanz          |
| D3DDECLTYPE \_ floatm   | D3DDECLUSAGE \_ texcoord     | n           | D3DFVF \_ texcoordsizem (n)  |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE- \_ Position     | 1           | Nicht zutreffend                       |
| D3DDECLTYPE \_ FLOAT3   | D3DDECLUSAGE \_ Normal       | 1           | Nicht zutreffend                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Deklaration](vertex-declaration.md)
</dt> </dl>

 

 



