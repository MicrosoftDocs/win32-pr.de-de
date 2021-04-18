---
description: Trennt die NPP vom Netzwerk.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats::D isconnect-Methode (Netmon. h)
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
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347720"
---
# <a name="istatsdisconnect-method"></a>IStats::D isconnect-Methode

Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>        | Der NPP erfasst derzeit Daten. Die Verbindung mit dem Netzwerk kann während der Datenerfassung nicht getrennt werden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>   | Der npp ist nicht mit dem Netzwerk verbunden.<br/>                                                                         |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl> | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**iStats:: Connect**](istats-connect.md) -Methode.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst. Nennen Sie zuerst die **iStats::D isconnect** -Methode, und klicken Sie dann auf [**iStats:: Beendigung**](istats-stop.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats:: Connect**](istats-connect.md)
</dt> <dt>

[**IStats:: Beendigung**](istats-stop.md)
</dt> </dl>

 

 




