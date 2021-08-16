---
description: Legt eine bestimmte Microsoft .NET Passport-Anmeldeoption fest.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92a1c432df3f3948a85205e26da64073722ba84dd365ebdcaccf3b80521c517c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827205"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3::p ut \_ Option-Methode

Legt eine bestimmte Microsoft .NET Passport-Anmeldeoption fest.

> [!Note]  
> Die **put \_ Option-Methode** gehört zur [**IPassportManager3-Schnittstelle.**](/previous-versions/ms817681(v=msdn.10)) Dieses Thema ergänzt die anfängliche Dokumentation.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Die festzulegende Anmeldeoption. Derzeit wird nur iMode unterstützt.

</dd> <dt>

*newVal* 
</dt> <dd>

Eine **VARIANT** (VT \_ BOOL), die den neuen Wert für die Option angibt. Dieser Wert kann True oder False sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode erfolgreich ist.

## <a name="remarks"></a>Hinweise

Diese Methode wird mit älteren Versionen des Passport SDK ausgeliefert.

 

 
