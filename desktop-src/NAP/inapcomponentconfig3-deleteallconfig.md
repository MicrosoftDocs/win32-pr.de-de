---
title: INapComponentConfig3 DeleteAllConfig-Methode (NapCommon.h)
description: Wird von System health validators (SHVs) implementiert, um eine Möglichkeit zu bieten, den SHV-Speicher nach dem Setup auf seinen ursprünglichen Zustand zurückzusetzen.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- DeleteAllConfig-Methode NAP
- DeleteAllConfig-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3-Schnittstelle NAP, DeleteAllConfig-Methode
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
ms.openlocfilehash: 05b2a81a33dfb659c3398c8c853132244d088b7fa65bd4bb0317869e13b85abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621739"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3::D eleteAllConfig-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **DeleteAllConfig-Methode** wird von System health validators (SHVs) implementiert, um eine Möglichkeit zu bieten, den SHV-Speicher nach dem Setup auf seinen ursprünglichen Zustand zurückzusetzen. Alle Konfigurationsdaten mit Ausnahme der Standardkonfiguration müssen gelöscht werden.

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
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





