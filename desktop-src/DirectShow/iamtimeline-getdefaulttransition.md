---
description: Die getdefaulttransition-Methode ruft den Standard Übergang ab. Wenn die Rendering-Engine einen Übergang nicht Renderingmodul renderten kann, ersetzt Sie den Standard Übergang
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Iamtimeline:: getdefaulttransition-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367736"
---
# <a name="iamtimelinegetdefaulttransition-method"></a>Iamtimeline:: getdefaulttransition-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetDefaultTransition` Methode ruft den Standard Übergang ab. Wenn die Rendering-Engine einen Übergang nicht Renderingmodul renderten kann, ersetzt Sie den Standard Übergang

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* 
</dt> <dd>

Empfängt die GUID des Standard Übergangs.

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

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




