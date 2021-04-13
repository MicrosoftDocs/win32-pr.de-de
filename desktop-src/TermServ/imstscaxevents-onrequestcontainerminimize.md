---
title: Imstscaxevents onrequestcontainerminimum-Methode
description: Wird aufgerufen, wenn der Benutzer auf der Verbindungs Leiste im Vollbildmodus auf die Schaltfläche Minimieren drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, dass die Containeranwendung sich selbst minimiert.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Onrequestcontainerminimi-Methode Remotedesktopdienste
- Onrequestcontainerminimi-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onrequestcontainerminimi-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392022"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>Imstscaxevents:: onrequestcontainerminimum-Methode

Wird aufgerufen, wenn der Benutzer auf der Verbindungs Leiste im Vollbildmodus auf die Schaltfläche **minimieren** drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, dass die Containeranwendung sich selbst minimiert.

## <a name="syntax"></a>Syntax


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird nur aufgerufen, wenn der im Container behandelte Vollbildmodus aktiviert ist. Weitere Informationen finden Sie unter [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





