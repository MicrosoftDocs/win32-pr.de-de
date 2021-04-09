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
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958176"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3::p UT- \_ options Methode

Legt eine bestimmte Microsoft .NET Passport-Anmeldeoption fest.

> [!Note]  
> Die **Put- \_ options** Methode gehört zur [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) -Schnittstelle. In diesem Thema wird die erste Dokumentation ergänzt.

 

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

Die festzulegende Anmeldeoption. Derzeit ist die einzige unterstützte Option iMode.

</dd> <dt>

*NewVal* 
</dt> <dd>

Ein **Variant** (VT \_ bool), der den neuen Wert für die Option angibt. Dieser Wert kann "true" oder "false" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode erfolgreich ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird mit älteren Versionen des Passport SDK ausgeliefert.

 

 
