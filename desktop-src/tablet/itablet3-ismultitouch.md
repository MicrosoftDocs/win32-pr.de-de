---
description: Bestimmt, ob ein Eingabegerät Multitouchscreen unterstützt.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'ITablet3:: ismultitouchscreen-Methode'
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
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217670"
---
# <a name="itablet3ismultitouch-method"></a>ITablet3:: ismultitouchscreen-Methode

Bestimmt, ob ein Eingabegerät Multitouchscreen unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bismultiberühren* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob das Gerät multiberühren ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück, andernfalls wird ein Fehlercode wie **z \_ . b**. "Fehler" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie über [**IRealTimeStylus3:: multitouchenabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) oder **ITablet3:: ismultiberühren** festgelegt haben, dass multiinput verfügbar ist, wählt eine Anwendung möglicherweise multifingereingabenachrichten aus. Weitere Informationen zum Filtern von multifingermethoden finden Sie im Abschnitt **IRealTimeStylus3:: multitouchenabled** -Eigenschaft.

## <a name="examples"></a>Beispiele


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




