---
description: Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: WIA. ontransfercomplete-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216059"
---
# <a name="wiaontransfercomplete-event"></a>WIA. ontransfercomplete-Ereignis

Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* 
</dt> <dd>

Das übermittelte [**Element**](-wia-item.md) Objekt.

</dd> <dt>

*Pfad* 
</dt> <dd>

Der Pfad und der Dateiname des übertragenen Bilds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

WIA benachrichtigt das Skript oder die Anwendung, wenn eine Datenübertragung, ein Bild oder ein Sound erfolgreich abgeschlossen wird. Implementieren Sie die **objwia** \_ **ontransfercomplete ()** -Unterroutine, damit das Skript oder die Anwendung auf den Abschluss der Datenübertragung reagieren kann.

Beispielsweise kann es sein, dass ein Skript nach der Übertragung ein Bild anzeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




