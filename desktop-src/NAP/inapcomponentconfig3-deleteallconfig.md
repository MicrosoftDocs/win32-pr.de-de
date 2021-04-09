---
title: INapComponentConfig3 deleteallconfig-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um den SHV-Speicher nach dem Setup in seinen ursprünglichen Zustand zurückzusetzen.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Deleteallconfig-Methode NAP
- Deleteallconfig-Methode, NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, deleteallconfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858776"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3::D eleteallconfig-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **deleteallconfig** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zu bieten, den SHV-Speicher nach dem Setup in seinen ursprünglichen Zustand zurückzusetzen. Alle Konfigurationsdaten außer der Standardkonfiguration müssen gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                           | Beschreibung                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Der Vorgang ist erfolgreich.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





