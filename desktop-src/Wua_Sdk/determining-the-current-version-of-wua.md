---
description: Bestimmen Sie die Version des Windows Update-Agents (WUA), bevor Sie sie verwenden.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Bestimmen der aktuellen Version von WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049498"
---
# <a name="determining-the-current-version-of-wua"></a>Bestimmen der aktuellen Version von WUA

Allgemeine Informationen zum Aktualisieren des WUA, einschließlich Schritt-für-Schritt-Anweisungen zum programmgesteuerten Bestimmen, ob die version of WUA, die auf dem Computer ausgeführt wird, Ihren Anforderungen entspricht, finden Sie unter Aktualisieren des [Windows Update-Agents](updating-the-windows-update-agent.md).

Bei Versionen von Windows vor Windows 7 und Windows Server 2008 R2 sollten Sie die installierte Version des Windows Update-Agents (WUA) ermitteln, bevor Sie sie verwenden. Die aktuelle Version von WUA wird durch die Version des Wuaueng.dll bestimmt, die im Unterverzeichnis System32 der aktuellen Windows \\ wird. Wenn die Version Wuaueng.dll Version 5.4.3790.1000 oder höher ist, wird WUA installiert. Eine Frühere Version als 5.4.3790.1000 gibt an, dass Softwareupdatedienste (SOFTWARE Update Services, SUS) 1.0 installiert sind.

Wenn sus 1.0 mithilfe der WUA-API aufgerufen wird, wird ein **HRESULT** von WU \_ E AU \_ \_ LEGACYSERVER zurückgegeben.

Sie können auch die [**IWindowsUpdateAgentInfo::GetInfo-Methode**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) verwenden, um die aktuelle Dateiversion von Wuapi.dll, die auf einem Computer ausgeführt wird, abzurufen. Die [**IWindowsUpdateAgentInfo-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) wird in WUA 1.0 nicht unterstützt.
