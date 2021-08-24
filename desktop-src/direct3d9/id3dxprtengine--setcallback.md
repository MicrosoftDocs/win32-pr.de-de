---
description: Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abgeschlossenen SH-Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubricht.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: ID3DXPRTEngine::SetCallBack-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1ed2570c45380ce4faa0be42ddb9231d6420940dd9a6d669d6f2540154dc644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847359"
---
# <a name="id3dxprtenginesetcallback-method"></a>ID3DXPRTEngine::SetCallBack-Methode

Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abgeschlossenen SH-Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCB* \[ In\]
</dt> <dd>

Typ: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Zeiger auf die [Rückruffunktion LPD3DXSHPRTSIMCB,](lpd3dxshprtsimcb.md) die den Prozentsatz der abgeschlossenen SH-Berechnungen berechnet. Die Rückruffunktion muss implementiert werden, um S \_ OK zurückzugeben, um den Simulator weiter auszuführen. Jeder andere Wert bricht den Simulator ab.

</dd> <dt>

*Häufigkeit* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Häufigkeit von Rückrufaufrufen. Die Umkehrung von Frequency entspricht ungefähr der Häufigkeit, mit der die Rückruffunktion aufgerufen wird.

</dd> <dt>

*lpUserContext* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist S \_ OK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
