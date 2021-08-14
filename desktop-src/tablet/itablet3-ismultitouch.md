---
description: Bestimmt, ob ein Eingabegerät Multitouch unterstützt.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: ITablet3::IsMultiTouch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: bbdd18d27c8b9f5f4b7567e6aa22fd0c74f5e2c2dc74d80e1f46aca4195b93ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717299"
---
# <a name="itablet3ismultitouch-method"></a>ITablet3::IsMultiTouch-Methode

Bestimmt, ob ein Eingabegerät Multitouch unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bIsMultiTouch* \[ out\]
</dt> <dd>

Gibt an, ob das Gerät multitouch ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück, andernfalls wird ein Fehlercode wie **E FAIL \_ zurückgegeben.**

## <a name="remarks"></a>Hinweise

Nachdem sie über [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) oder **ITablet3::IsMultiTouch** ermittelt haben, dass Multitouch verfügbar ist, kann eine Anwendung multitouch-Eingabenachrichten auswählen. Weitere Informationen zum Filtern von Multitouch-Methoden finden Sie im Eigenschaftenabschnitt **IRealTimeStylus3::MultiTouchEnabled.**

## <a name="examples"></a>Beispiele


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




