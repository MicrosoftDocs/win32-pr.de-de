---
description: Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die MsiNTSuiteDataCenter-Eigenschaft auf 1 fest, wenn Windows 2000 Datacenter Server installiert ist.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: MsiNTSuiteDataCenter-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b42edc0a4abb544133b4b7fb176988f826c5af172cc4c0d49ca56494ed37672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082810"
---
# <a name="msintsuitedatacenter-property"></a>MsiNTSuiteDataCenter-Eigenschaft

Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die **MsiNTSuiteDataCenter-Eigenschaft** auf 1 fest, wenn Windows 2000 Datacenter Server installiert ist. Das Installationsprogramm legt diese Eigenschaft nur auf 1 fest, wenn das VER \_ SUITE \_ DATACENTER-Flag in der [**OSVERSIONINFOEX-Struktur**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) festgelegt ist. Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
