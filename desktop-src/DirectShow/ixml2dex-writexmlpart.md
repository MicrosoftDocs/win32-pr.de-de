---
description: 'IXml2Dex::WriteXMLPart-Methode: Nicht implementiert.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: IXml2Dex::WriteXMLPart-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: a9ca563c0c780b9c2f4d2171fdaa9e365b15a3b014ec4c4a42a28de7b43f3f3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397561"
---
# <a name="ixml2dexwritexmlpart-method"></a>IXml2Dex::WriteXMLPart-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Nicht implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimeline* 
</dt> <dd>

Reserviert.

</dd> <dt>

*dStart* 
</dt> <dd>

Reserviert.

</dd> <dt>

*dEnd* 
</dt> <dd>

Reserviert.

</dd> <dt>

*FileName* 
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IXml2Dex-Schnittstelle**](ixml2dex.md)
</dt> </dl>

 

 



