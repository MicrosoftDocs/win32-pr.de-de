---
description: Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Wia.OnTransferComplete-Ereignis
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
ms.openlocfilehash: 9095302a2f3fe75e1939ebb979ec4aad4d87b0462a5b40997e5523e7313d98e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209274"
---
# <a name="wiaontransfercomplete-event"></a>Wia.OnTransferComplete-Ereignis

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

Das übertragene [**Item-Objekt.**](-wia-item.md)

</dd> <dt>

*Path* 
</dt> <dd>

Der Pfad und der Dateiname des übertragenen Images.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

WIA benachrichtigt das Skript oder die Anwendung, wenn eine Datenübertragung, ein Bild oder ein Sound erfolgreich abgeschlossen wurde. Implementieren Sie die **ObjWia** \_ **OnTransferComplete()-Unterroutine,** damit Ihr Skript oder Ihre Anwendung auf den Abschluss der Datenübertragung reagieren kann.

Angenommen, Sie möchten, dass ein Skript ein Bild anzeigt, nachdem es übertragen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




