---
description: Ruft den Wert einer bestimmten Microsoft .NET Passport-Anmeldeoption ab.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'IPassportManager3:: get_option-Methode'
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
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392930"
---
# <a name="ipassportmanager3get_option-method"></a>IPassportManager3:: get- \_ options Methode

Ruft den Wert einer bestimmten Microsoft .NET Passport-Anmeldeoption ab.

> [!Note]  
> Die Methode **get \_ Option** gehört zur [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) -Schnittstelle. In diesem Thema wird die erste Dokumentation ergänzt.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Die abzurufende Anmeldeoption. Derzeit ist die einzige unterstützte Option "iMode".

</dd> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **Variant** (VT \_ bool), der den Wert der Option empfängt. Dieser Wert kann "true" oder "false" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode erfolgreich ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird mit älteren Versionen des Passport SDK ausgeliefert.

 

 
