---
description: Die Time-Eigenschaft ist die aktuelle Zeit in Stunden, Minuten und Sekunden als Zeichenfolge von Literaltext im Format HH:MM:SS mit einer 24-Stunden-Uhr.
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Time-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050d6897b966017a18241ed7e0374174e5343f48f16e311923b1c7564f012681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141792"
---
# <a name="time-property"></a>Time-Eigenschaft

Die **Time-Eigenschaft** ist die aktuelle Zeit in Stunden, Minuten und Sekunden als Zeichenfolge von Literaltext im Format HH:MM:SS mit einer 24-Stunden-Uhr. Beispiel: Die Uhrzeit 18:57 Uhr wird durch "18:57:00" dargestellt. Das Format des Werts hängt vom Gebietsschema des Benutzers ab und ist das Format, das mithilfe der [**GetTimeFormat-Funktion**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) mit der \_ TIME FORCE24HOURFORMAT \| TIME \_ NOTIMEMARKER-Option abgerufen wird. Der Wert dieser Eigenschaft wird vom Windows Installer und nicht vom Paketautor festgelegt.

## <a name="remarks"></a>Hinweise

Da es sich um eine Textzeichenfolge handelt, kann sie nicht in bedingten Ausdrücken verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
