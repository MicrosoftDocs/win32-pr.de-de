---
description: Tritt auf, wenn sich der Inhalt des InkEdit-Steuer Elements ändert.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: InkEdit. Change-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373254"
---
# <a name="inkeditchange-event"></a>InkEdit. Change-Ereignis

Tritt auf, wenn sich der Inhalt des [InkEdit](inkedit-control-reference.md) -Steuer Elements ändert.

## <a name="syntax"></a>Syntax


```C++
void Change();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt auf, wenn Eigenschaften, die sich auf den Inhalt des [InkEdit](inkedit-control-reference.md) -Steuer Elements auswirken, geändert werden.

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner " **DISPID \_ ieechange**".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




