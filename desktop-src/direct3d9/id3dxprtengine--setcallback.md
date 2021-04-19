---
description: Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abzurufenden sphärischen (SH) Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubrechen.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine:: SetCallback-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350698"
---
# <a name="id3dxprtenginesetcallback-method"></a>ID3DXPRTEngine:: SetCallback-Methode

Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abzurufenden sphärischen (SH) Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubrechen.

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

*Platine* \[ in\]
</dt> <dd>

Typ: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Ein Zeiger auf die [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) -Rückruffunktion, die den Prozentsatz der abgeschlossenen SH-Berechnungen berechnet. Die Rückruffunktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um den Simulator weiterhin ausführen zu können. Bei jedem anderen Wert wird der Simulator abgebrochen.

</dd> <dt>

*Häufigkeit* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Häufigkeit von Rückruf aufrufen. Die Umkehrung der Häufigkeit entspricht ungefähr der Häufigkeit, mit der die Rückruffunktion aufgerufen wird.

</dd> <dt>

*lpusercontext* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übermittelt wird. Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist "S \_ OK".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
