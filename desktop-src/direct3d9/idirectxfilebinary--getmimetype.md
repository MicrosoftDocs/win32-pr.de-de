---
description: Ruft den Multipurpose Internet Mail Extensions (MIME)-Typ für die Binärdaten ab. Veraltet.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Idirectxfilebinary:: getmimetype-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961588"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>Idirectxfilebinary:: getmimetype-Methode

Ruft den Multipurpose Internet Mail Extensions (MIME)-Typ für die Binärdaten ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszmimetype* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Adresse eines Zeigers, der die MIME-Typzeichenfolge empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.

## <a name="remarks"></a>Bemerkungen

Wenn kein MIME-Typ in einer DirectX-Datei für ein binäres Objekt angegeben ist, legt die Funktion pszmimetype auf **null** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfilebinary](idirectxfilebinary.md)
</dt> </dl>

 

 
