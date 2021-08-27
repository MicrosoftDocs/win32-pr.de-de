---
description: Trennt die Verbindung zwischen dem NPP und dem Netzwerk.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats::D isconnect-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: eabba7b5cf234d48b2839074ec1ad07380a7ed14858f6bd43b07f7d2eaa033b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037190"
---
# <a name="istatsdisconnect-method"></a>IStats::D isconnect-Methode

Die **Disconnect-Methode** trennt den Netzwerk-NPP vom Netzwerk.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>        | Das NPP erfasst derzeit Daten. Sie können die Verbindung mit dem Netzwerk nicht trennen, während eine Datenerfassung in Bearbeitung ist.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>   | Der NPP ist nicht mit dem Netzwerk verbunden.<br/>                                                                         |
| <dl> <dt>**NMERR \_ NICHT \_ NUR STATISTIKEN \_**</dt> </dl> | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [**IStats::Verbinden-Methode.**](istats-connect.md)<br/>          |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst. Rufen Sie **zuerst die IStats::D isconnect-Methode** und dann [**IStats::Stop auf.**](istats-stop.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::Verbinden**](istats-connect.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 




