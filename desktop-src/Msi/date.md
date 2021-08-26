---
description: Die Date-Eigenschaft ist der aktuelle Monat, Der aktuelle Tag und das aktuelle Jahr als Zeichenfolge mit Literaltext im Format MM/TT/YYYY.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf76df99c5567351ddd4d36d1aaad56c8a4d1f385f21ca977a4d54916ce99a4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129630"
---
# <a name="date-property"></a>Date-Eigenschaft

Die **Date-Eigenschaft** ist der aktuelle Monat, Der aktuelle Tag und das aktuelle Jahr als Zeichenfolge mit Literaltext im Format MM/TT/YYYY. Beispielsweise kann das Datum 22. Juni 2005 als "22.06.2005" dargestellt werden. Das Format des Werts hängt vom Benutzer-Locale ab und ist das Format, das mit [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) mit der DATE \_ SHORTDATE-Option ermittelt wird. Der Wert dieser Eigenschaft wird vom Windows Installer und nicht vom Paketautor festgelegt.

## <a name="remarks"></a>Hinweise

Da es sich um eine Textzeichenfolge handelt, kann sie nicht in bedingten Ausdrücken verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

