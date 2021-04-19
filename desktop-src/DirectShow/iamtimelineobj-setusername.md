---
description: Die setUserName-Methode legt einen von der Anwendung definierten Namen für das Objekt fest.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'Iamtimelineobj:: setUserName-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372640"
---
# <a name="iamtimelineobjsetusername-method"></a>Iamtimelineobj:: setUserName-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetUserName` -Methode legt einen Anwendungs definierten Namen für das-Objekt fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* 
</dt> <dd>

Zeichenfolge mit breit Zeichen, die den Namen enthält. Zeichen folgen, die länger als 256 Zeichen sind, werden möglicherweise abgeschnitten.

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

 

 




