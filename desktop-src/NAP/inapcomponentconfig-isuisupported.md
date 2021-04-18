---
title: Inapcomponentconfig isuisupported-Methode (napcommon. h)
description: Gibt an, ob die Komponente eine angepasste Benutzeroberfläche unterstützt.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Isuisupported-Methode NAP
- Isuisupported-Methode, NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, isuisupported-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337324"
---
# <a name="inapcomponentconfigisuisupported-method"></a>Inapcomponentconfig:: isuisupported-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **isuisupported** -Methode gibt an, ob die Komponente eine angepasste Benutzeroberfläche unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsSupported* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen booleschen Wert, der auf **true** festgelegt ist, wenn die Komponente eine angepasste Benutzeroberfläche unterstützt, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die angepasste Benutzeroberfläche einer Komponente sollte mithilfe von [**inapcomponentconfig:: invokeui**](inapcomponentconfig-invokeui.md)gestartet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapcomponentconfig**](inapcomponentconfig.md)
</dt> <dt>

[**Inapcomponentconfig:: invokeui**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





