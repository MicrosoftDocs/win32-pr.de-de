---
description: Ruft Schriftartmerkmale ab.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: ID3DX10Font::GetTextMetrics-Methode (D3DX10.h)
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
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047048"
---
# <a name="id3dx10fontgettextmetrics-method"></a>ID3DX10Font::GetTextMetrics-Methode

Ruft Schriftartmerkmale ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTextMetrics* \[ In\]
</dt> <dd>

Typ: **TEXTMETRIC \***

Zeiger auf eine [TEXTMETRIC-Struktur,](/previous-versions//ms534202(v=vs.85)) die Schriftarteigenschaften enthält. Wenn Unicode definiert ist, gibt die Funktion eine TEXTMETRICW-Struktur zurück. Andernfalls gibt die Funktion eine TEXTMETRICA-Struktur zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Ist ungleich null (0), wenn die Funktion erfolgreich ausgeführt wird, andernfalls null (0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
