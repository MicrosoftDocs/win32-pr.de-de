---
description: Rufen Sie Schriftart Eigenschaften ab.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font:: GetTextMetrics-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530938"
---
# <a name="id3dx10fontgettextmetrics-method"></a>ID3DX10Font:: GetTextMetrics-Methode

Rufen Sie Schriftart Eigenschaften ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptextmetrics* \[ in\]
</dt> <dd>

Typ: **TextMetric \***

Zeiger auf eine [textmetrikstruktur](/previous-versions//ms534202(v=vs.85)) , die Schriftart Eigenschaften enthält. Wenn Unicode definiert ist, gibt die Funktion eine textmetricw-Struktur zurück. Andernfalls gibt die Funktion eine textmetrica-Struktur zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Ist ungleich null (0), wenn die Funktion erfolgreich ausgeführt wird, andernfalls null (0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
