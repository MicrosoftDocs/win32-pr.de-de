---
description: Ruft den Wert einer bestimmten Microsoft .NET Passport-Anmeldeoption ab.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: IPassportManager3::get_Option-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5d7260e3c13be21f1cc963e1bca15a6126739a0075b94ee11f07d98901efd39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750040"
---
# <a name="ipassportmanager3get_option-method"></a>IPassportManager3::get \_ Option-Methode

Ruft den Wert einer bestimmten Microsoft .NET Passport-Anmeldeoption ab.

> [!Note]  
> Die **get \_ Option-Methode** gehört zur [**IPassportManager3-Schnittstelle.**](/previous-versions/ms817681(v=msdn.10)) Dieses Thema ergänzt die erste Dokumentation.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Die abzurufende Anmeldeoption. Derzeit wird nur die Option "iMode" unterstützt.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **VARIANT** (VT \_ BOOL), die den Wert der Option empfängt. Dieser Wert kann True oder False sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode erfolgreich ist.

## <a name="remarks"></a>Hinweise

Diese Methode wird mit älteren Versionen des Passport SDK bereitgestellt.

 

 
