---
description: Die Date-Eigenschaft entspricht dem aktuellen Monat, Tag und Jahr als Zeichenfolge mit Literaltext im Format mm/dd/yyyy.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359667"
---
# <a name="date-property"></a>Date-Eigenschaft

Die **Date** -Eigenschaft entspricht dem aktuellen Monat, Tag und Jahr als Zeichenfolge mit Literaltext im Format mm/dd/yyyy. Beispielsweise kann das Datum 22. Juni 2005 als "06/22/2005" dargestellt werden. Das Format des Werts hängt vom Gebiets Schema des Benutzers ab. dabei handelt es sich um das Format, das mithilfe von [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) mit der \_ Option Datum SHORTDATE abgerufen wird. Der Wert dieser Eigenschaft wird vom Windows Installer und nicht vom Paket Ersteller festgelegt.

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

 

