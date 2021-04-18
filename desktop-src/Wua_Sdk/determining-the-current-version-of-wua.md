---
description: Bestimmen Sie die Version von Windows Update-Agent (WUA), bevor Sie Sie verwenden.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Ermitteln der aktuellen WUA-Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347307"
---
# <a name="determining-the-current-version-of-wua"></a>Ermitteln der aktuellen WUA-Version

Allgemeine Informationen zum Aktualisieren von WUA, einschließlich Schritt-für-Schritt-Anweisungen zur programmgesteuerten Ermittlung von innerhalb Ihrer APP, unabhängig davon, ob die auf dem Computer laufende Version von WUA Ihren Anforderungen entspricht, finden Sie unter [Aktualisieren des Windows Update-Agents](updating-the-windows-update-agent.md).

Unter Windows-Versionen vor Windows 7 und Windows Server 2008 R2 sollten Sie die installierte Version von Windows Update-Agent (WUA) bestimmen, bevor Sie Sie verwenden. Die aktuelle Version von WUA wird durch die Version der Wuaueng.dll bestimmt, die im \\ Unterverzeichnis System32 der aktuellen Windows-Installation ausgeführt wird. Wenn die Version von Wuaueng.dll Version 5.4.3790.1000 oder eine höhere Version ist, wird WUA installiert. Eine frühere Version als 5.4.3790.1000 gibt an, dass Software Update Services (SUS) 1,0 installiert ist.

Wenn Sie SUS 1,0 mithilfe der WUA-API aufruft, wird ein **HRESULT** von Wu \_ E \_ au \_ Legacyserver zurückgegeben.

Sie können auch die [**iwindowsupdateagentinfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) -Methode verwenden, um die aktuelle Dateiversion von Wuapi.dll abzurufen, die auf einem Computer ausgeführt wird. Die [**iwindowsupdateagentinfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) -Schnittstelle wird in WUA 1,0 nicht unterstützt.
