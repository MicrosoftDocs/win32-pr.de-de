---
description: Ruft die Gitter Optionen ab, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert sind.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh:: GetOptions-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373535"
---
# <a name="id3dxbasemeshgetoptions-method"></a>ID3DXBaseMesh:: GetOptions-Methode

Ruft die Gitter Optionen ab, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert sind.

## <a name="syntax"></a>Syntax


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt eine Kombination aus einem oder mehreren der folgenden Flags zurück, die die Optionen angibt, die für dieses Mesh zum Zeitpunkt der Erstellung aktiviert wurden.



| Wert                   | BESCHREIBUNG                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32-Bit         | Verwenden Sie 32-Bit-Indizes.                                                                                                                                                                              |
| D3DXMESH \_ DoNotClip     | Verwenden Sie das D3DUSAGE \_ DoNotClip-nutzungsflag für Scheitelpunkt-und Index Puffer.                                                                                                                             |
| D3DXMESH \_ dynamisch       | Äquivalent zum Angeben von D3DXMESH \_ vb \_ Dynamic und D3DXMESH \_ IB \_ Dynamic.                                                                                                                   |
| D3DXMESH \_ rtpatches     | Verwenden Sie das D3DUSAGE \_ rtpatches Usage-Flag für Scheitelpunkt-und Index Puffer.                                                                                                                             |
| D3DXMESH \_ npatches      | Die Angabe dieses Flags bewirkt, dass der Scheitelpunkt und der Index Puffer des Mesh mit dem D3DUSAGE \_ npatches-Flag erstellt werden. Dies ist erforderlich, wenn das Mesh-Objekt mit der N-Patch-Erweiterung gerendert werden soll. |
| D3DXMESH \_ verwaltet       | Entspricht der Angabe von D3DXMESH \_ vb \_ Managed und D3DXMESH \_ IB \_ Managed.                                                                                                                   |
| D3DXMESH \_ Punkte        | Verwenden Sie das \_ Usage-Flag D3DUSAGE Points für Scheitelpunkt-und Index Puffer.                                                                                                                                |
| D3DXMESH \_ IB \_ dynamisch   | Verwenden Sie das D3DUSAGE \_ Dynamic Usage-Flag für Index Puffer.                                                                                                                                          |
| D3DXMESH \_ IB \_ verwaltet   | Verwenden Sie die \_ verwaltete D3DPOOL-Speicher Klasse für Index Puffer.                                                                                                                                         |
| D3DXMESH \_ IB-System Arbeitsspeicher \_ | Verwenden Sie die D3DPOOL \_ SystemMem-Speicher Klasse für Index Puffer.                                                                                                                                       |
| D3DXMESH \_ IB \_ schreibgeschützt | Verwenden Sie das D3DUSAGE \_ Write-use-Flag für Index Puffer.                                                                                                                                        |
| D3DXMESH \_ SystemMem     | Entspricht der Angabe von D3DXMESH \_ vb \_ SystemMem und D3DXMESH \_ IB \_ SystemMem.                                                                                                               |
| D3DXMESH \_ vb \_ dynamisch   | Verwenden Sie das D3DUSAGE \_ Dynamic Usage-Flag für Scheitelpunkt Puffer.                                                                                                                                         |
| D3DXMESH \_ vb \_ verwaltet   | Verwenden Sie die \_ verwaltete D3DPOOL-Speicher Klasse für Scheitelpunkt Puffer.                                                                                                                                        |
| D3DXMESH \_ vb \_ SystemMem | Verwenden Sie die D3DPOOL \_ SystemMem-Speicher Klasse für Scheitelpunkt Puffer.                                                                                                                                      |
| D3DXMESH \_ vb \_ schreibgeschützt | Verwenden Sie das D3DUSAGE \_ Write-use-Flag für Scheitel Punkte.                                                                                                                                       |
| D3DXMESH \_ schreiben     | Entspricht der Angabe von D3DXMESH \_ vb \_ Write-only und D3DXMESH \_ IB \_ Write.                                                                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
