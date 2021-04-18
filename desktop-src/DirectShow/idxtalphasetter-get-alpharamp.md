---
description: Die get \_ alpharamp-Methode ruft die Eigenschaft für die Alpha-Eigenschaft ab. Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Idxtalphasetter:: get_AlphaRamp-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351270"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>Idxtalphasetter:: get \_ alpharamp-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_AlphaRamp` Methode ruft die Eigenschaft für die Alpha-Eigenschaft ab. Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Palpha* \[ Out, retval\]
</dt> <dd>

Empfängt die Alpha-Rampe. Ein negativer Wert gibt an, dass keine Alpha-Rampe festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                               | Beschreibung                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idxtalphasetter-Schnittstelle**](idxtalphasetter.md)
</dt> </dl>

 

 




