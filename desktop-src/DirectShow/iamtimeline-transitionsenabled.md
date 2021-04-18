---
description: Die transitionsenabled-Methode bestimmt, ob Übergänge aktiviert sind.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'Iamtimeline:: transitionsenabled-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360923"
---
# <a name="iamtimelinetransitionsenabled-method"></a>Iamtimeline:: transitionsenabled-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **transitionsenabled** -Methode bestimmt, ob Übergänge aktiviert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfaktivierte* 
</dt> <dd>

Empfängt einen booleschen Wert. **True** gibt an, dass Übergänge aktiviert sind. Andernfalls sind Übergänge deaktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[**Iamtimeline:: enabletransitions**](iamtimeline-enabletransitions.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




