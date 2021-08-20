---
title: INapComponentConfig IsUISupported-Methode (NapCommon.h)
description: Gibt an, ob die Komponente eine benutzerdefinierte Benutzeroberfläche unterstützt.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- IsUISupported-Methode NAP
- IsUISupported-Methode NAP, INapComponentConfig-Schnittstelle
- INapComponentConfig-Schnittstelle NAP , IsUISupported-Methode
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
ms.openlocfilehash: 5e343b037e4f77b4c1e342ffa78278854b11d714e09e9e57188d83fc9f93a180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134488"
---
# <a name="inapcomponentconfigisuisupported-method"></a>INapComponentConfig::IsUISupported-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **IsUISupported-Methode** gibt an, ob die Komponente eine benutzerdefinierte Benutzeroberfläche unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isSupported* \[ out\]
</dt> <dd>

Ein Zeiger auf eine BOOL, die auf **TRUE** festgelegt ist, wenn die Komponente eine angepasste Benutzeroberfläche unterstützt, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die benutzerdefinierte Benutzeroberfläche einer Komponente sollte mit [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)gestartet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





