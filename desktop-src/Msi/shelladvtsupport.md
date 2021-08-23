---
description: Die ShellAdvtSupport-Eigenschaft wird vom Installationsprogramm festgelegt, wenn die IShellLink-Schnittstelle des Systems die Auflösung des Installerdeskriptors unterstützt.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: ShellAdvtSupport-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfacc34bfffdde9ce34841030f38c443a243c9923cb70749a27615cccc1c676e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628440"
---
# <a name="shelladvtsupport-property"></a>ShellAdvtSupport-Eigenschaft

Die **ShellAdvtSupport-Eigenschaft** wird vom Installationsprogramm festgelegt, wenn die [**IShellLink-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) des Systems die Auflösung des Installerdeskriptors unterstützt.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft festgelegt ist, unterstützt die [**IShellLink-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) des Systems die Auflösung des Installerdeskriptors. Dies wird von Windows 2000 und Systemen mit Internet Explorer 4.01 unterstützt. Wenn diese Eigenschaft nicht festgelegt ist, hat das Installationsprogramm das Standardverhalten, während der Installation nicht angekündigte Features zu erstellen, entweder lokal oder von der Quelle aus ausgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Plattformunterstützung von Ankündigungen](platform-support-of-advertisement.md)
</dt> </dl>

 

 
