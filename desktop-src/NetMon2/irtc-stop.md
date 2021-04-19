---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'Untc:: stopmethode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345280"
---
# <a name="irtcstop-method"></a>Untc:: stopmethode

Die Methode " **Beenden** " beendet die aktuelle Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden. Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl> | Der NPP erfasst keine Daten. Wenden Sie zum Starten der Erfassung den Befehl " [irren:: Start](irtc-start.md) " an.<br/>                            |
| <dl> <dt>**nmerr \_ nicht in \_ Echtzeit**</dt> </dl>  | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Erfassung nach dem Aufrufen der Methode " **untc:: beenden** " neu starten, müssen Sie bei jedem Aufrufen von " [untc:: Start](irtc-start.md) " den Befehl " [iritc:: Configure](irtc-configure.md) " aufrufen, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Iran"](irtc.md)
</dt> <dt>

[Iran:: Connect](irtc-connect.md)
</dt> <dt>

["Iran:: Configure"](irtc-configure.md)
</dt> <dt>

["Iran:: Start"](irtc-start.md)
</dt> </dl>

 

 




