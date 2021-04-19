---
description: 'Die getdefaultfps-Methode ruft die Standardausgabe Frame Rate in Frames pro Sekunde (fps) ab. Gruppen verwenden diesen Wert als Standard Frame Rate. Um die Framerate einer Gruppe festzulegen, müssen Sie die iamtimelinegroup:: setoutputfps-Methode für die Gruppe aufrufen.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Iamtimeline:: getdefaultfps-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358373"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Iamtimeline:: getdefaultfps-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetDefaultFPS` Methode ruft die Standardausgabe Frame Rate in Frames pro Sekunde (fps) ab. Gruppen verwenden diesen Wert als Standard Frame Rate. Um die Framerate einer Gruppe festzulegen, müssen Sie die [**iamtimelinegroup:: setoutputfps**](iamtimelinegroup-setoutputfps.md) -Methode für die Gruppe aufrufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfps* 
</dt> <dd>

Empfängt die Standardbildrate in Frames pro Sekunde.

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

 

 




