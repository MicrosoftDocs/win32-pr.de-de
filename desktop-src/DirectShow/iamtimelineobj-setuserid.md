---
description: Die setuserid-Methode legt einen von der Anwendung definierten Bezeichner für das-Objekt fest.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'Iamtimelineobj:: setuserid-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365707"
---
# <a name="iamtimelineobjsetuserid-method"></a>Iamtimelineobj:: setuserid-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetUserID` -Methode legt einen von der Anwendung definierten Bezeichner für das-Objekt fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* 
</dt> <dd>

Der-Wert, der den Bezeichner angibt. Dieser Bezeichner wird nur von der Anwendung verwendet und kann ein beliebiger Wert sein.

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




