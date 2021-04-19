---
description: Die shelladvtsupport-Eigenschaft wird vom Installationsprogramm festgelegt, wenn die IShellLink-Schnittstelle des Systems die installerdeskriptorauflösung unterstützt.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Shelladvtsupport (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373583"
---
# <a name="shelladvtsupport-property"></a>Shelladvtsupport (Eigenschaft)

Die **shelladvtsupport** -Eigenschaft wird vom Installationsprogramm festgelegt, wenn die [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle des Systems die installerdeskriptorauflösung unterstützt.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft festgelegt ist, unterstützt die [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle des Systems die installerdeskriptorauflösung. Dies wird von Windows 2000 und Systemen unterstützt, die Internet Explorer 4,01 ausführen. Wenn diese Eigenschaft nicht festgelegt ist, hat das Installationsprogramm das Standardverhalten, dass während der Installation nicht angekündigte Features erstellt werden, entweder lokal oder von der Quelle aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Platt Form Unterstützung für Ankündigungen](platform-support-of-advertisement.md)
</dt> </dl>

 

 
