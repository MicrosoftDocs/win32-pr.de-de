---
description: Mit der setUserData-Methode werden von der Anwendung definierte persistente Daten festgelegt.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'Iamtimelineobj:: setUserData-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367720"
---
# <a name="iamtimelineobjsetuserdata-method"></a>Iamtimelineobj:: setUserData-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetUserData` -Methode legt von der Anwendung definierte persistente Daten fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Zeiger auf einen Puffer, der die Daten enthält.

</dd> <dt>

*Größe* 
</dt> <dd>

Größe der Daten in Bytes.

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

 

 




