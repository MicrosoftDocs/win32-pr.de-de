---
description: 'Die Time-Eigenschaft ist die aktuelle Zeit in Stunden, Minuten und Sekunden als eine Zeichenfolge mit Literaltext im Format hh: mm: SS, wobei eine 24-Stunden-Uhrzeit verwendet wird.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Time-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371415"
---
# <a name="time-property"></a>Time-Eigenschaft

Die **time** -Eigenschaft ist die aktuelle Zeit in Stunden, Minuten und Sekunden als eine Zeichenfolge mit Literaltext im Format hh: mm: SS, wobei eine 24-Stunden-Uhrzeit verwendet wird. Beispielsweise die Uhrzeit 6:57 Uhr wird durch "18:57:00" dargestellt. Das Format des Werts hängt vom Gebiets Schema des Benutzers ab. es ist das Format, das mit der [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) -Funktion mit der \_ Option Time FORCE24HOURFORMAT \| time \_ notimemarker abgerufen wird. Der Wert dieser Eigenschaft wird vom Windows Installer und nicht vom Paket Ersteller festgelegt.

## <a name="remarks"></a>Bemerkungen

Da es sich hierbei um eine Text Zeichenfolge handelt, kann Sie nicht in bedingten Ausdrücken verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
