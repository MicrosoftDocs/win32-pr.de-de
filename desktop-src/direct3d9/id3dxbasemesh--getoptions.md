---
description: Ruft die Gitternetzoptionen ab, die zum Zeitpunkt der Erstellung für dieses Gitternetz aktiviert sind.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: ID3DXBaseMesh::GetOptions-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b8ed6281e1418246027a05f281ef5c01d8fbe757a8bd88d2bf6f44ca41ed1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121762"
---
# <a name="id3dxbasemeshgetoptions-method"></a>ID3DXBaseMesh::GetOptions-Methode

Ruft die Gitternetzoptionen ab, die zum Zeitpunkt der Erstellung für dieses Gitternetz aktiviert sind.

## <a name="syntax"></a>Syntax


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt eine Kombination aus einem oder mehreren der folgenden Flags zurück, die die Optionen angeben, die für dieses Gitternetz zur Erstellungszeit aktiviert sind.



| Wert                   | Beschreibung                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32 BIT         | Verwenden Sie 32-Bit-Indizes.                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | Verwenden Sie das D3DUSAGE \_ DONOTCLIP-Verwendungsflag für Scheitelpunkt- und Indexpuffer.                                                                                                                             |
| D3DXMESH \_ DYNAMIC       | Entspricht der Angabe von D3DXMESH \_ VB \_ DYNAMIC und D3DXMESH \_ IB \_ DYNAMIC.                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | Verwenden Sie das D3DUSAGE \_ RTPATCHES-Verwendungsflag für Scheitelpunkt- und Indexpuffer.                                                                                                                             |
| D3DXMESH \_ NPATCHES      | Wenn Sie dieses Flag angeben, werden der Scheitelpunkt und der Indexpuffer des Gitternetzes mit dem NPATCHES-Flag D3DUSAGE \_ erstellt. Dies ist erforderlich, wenn das Gittermodellobjekt mithilfe der N-Patch-Erweiterung gerendert werden soll. |
| D3DXMESH \_ VERWALTET       | Entspricht der Angabe von D3DXMESH \_ VB \_ MANAGED und D3DXMESH \_ IB \_ MANAGED.                                                                                                                   |
| D3DXMESH-PUNKTE \_        | Verwenden Sie das D3DUSAGE \_ POINTS-Verwendungsflag für Scheitelpunkt- und Indexpuffer.                                                                                                                                |
| D3DXMESH \_ IB \_ DYNAMIC   | Verwenden Sie das D3DUSAGE \_ DYNAMIC-Verwendungsflag für Indexpuffer.                                                                                                                                          |
| D3DXMESH \_ IB \_ VERWALTET   | Verwenden Sie die \_ VERWALTETE D3DPOOL-Speicherklasse für Indexpuffer.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Verwenden Sie die D3DPOOL \_ SYSTEMMEM-Speicherklasse für Indexpuffer.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Verwenden Sie das D3DUSAGE \_ WRITEONLY-Verwendungsflag für Indexpuffer.                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | Entspricht der Angabe von D3DXMESH \_ VB \_ SYSTEMMEM und D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ DYNAMIC   | Verwenden Sie das D3DUSAGE \_ DYNAMIC-Verwendungsflag für Scheitelpunktpuffer.                                                                                                                                         |
| D3DXMESH \_ VB \_ VERWALTET   | Verwenden Sie die \_ VERWALTETE D3DPOOL-Speicherklasse für Scheitelpunktpuffer.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Verwenden Sie die D3DPOOL \_ SYSTEMMEM-Speicherklasse für Scheitelpunktpuffer.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Verwenden Sie das D3DUSAGE \_ WRITEONLY-Verwendungsflag für Scheitelpunktpuffer.                                                                                                                                       |
| D3DXMESH \_ WRITEONLY     | Entspricht der Angabe von D3DXMESH \_ VB \_ WRITEONLY und D3DXMESH \_ IB \_ WRITEONLY.                                                                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
