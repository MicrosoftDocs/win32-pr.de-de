---
description: Die get \_ Alpha-Methode ruft den Alpha-Wert für das gesamte Bild ab.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Idxtalphasetter:: get_Alpha-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367013"
---
# <a name="idxtalphasetterget_alpha-method"></a>Idxtalphasetter:: get \_ Alpha-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_Alpha` Methode ruft den Alpha-Wert für das gesamte Bild ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Palpha* \[ Out, retval\]
</dt> <dd>

Empfängt den Alpha-Wert. Dieser Alpha Wert wird auf das gesamte Zielbild angewendet. Ein negativer Wert gibt an, dass kein Alpha Wert festgelegt ist.

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

 

 




