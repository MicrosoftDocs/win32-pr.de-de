---
title: Run-Time Verknüpfen mit Wtsapi32.dll
description: Ihre Anwendung kann die Remotedesktopdienste-API verwenden, um zur Laufzeit dynamisch mit dem Wtsapi32.dll zu verknüpfen. Zu diesem Zweck sollte Ihre Anwendung die LoadLibrary-Funktion aufrufen, um Wtsapi32.dll zu laden.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc686f26029ee9bfa4332215e27a587a7e57b78de9bd0d1043ee58541ef76194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127495"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time Verknüpfen mit Wtsapi32.dll

Wenn Ihre Anwendung in einer Umgebung ausgeführt wird, die keine Remotedesktopdienste Umgebung ist, Aber Sie möchten, dass Ihre Anwendung zusätzliche Funktionen bereitstellt, wenn sie in einer Remotedesktopdienste Umgebung ausgeführt wird, kann die Anwendung die Remotedesktopdienste-API verwenden, um die zusätzliche Funktionalität zu implementieren, und zur Laufzeit dynamisch mit dem Wtsapi32.dll verknüpfen. Zu diesem Zweck sollte Ihre Anwendung die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufrufen, um Wtsapi32.dll zu laden. Wenn der **LoadLibrary-Aufruf** fehlschlägt, kann Ihre Anwendung mithilfe der grundlegenden Funktionalität ausgeführt werden. Wenn **LoadLibrary** erfolgreich ist, kann Ihre Anwendung die [**GetProcAddress-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen, um Zeiger auf die Remotedesktopdienste Funktionen abzurufen, die Sie aufrufen möchten.

Wenn Ihre Anwendung nur für eine Remotedesktopdienste-Umgebung vorgesehen ist, ist keine dynamische Verknüpfung erforderlich. In diesem Fall können Sie Wtsapi32.h einschließen und mit Wtsapi32.lib verknüpfen. Wenn Ihre Anwendung dann in einer anderen Umgebung als Remotedesktopdienste gestartet wird, wird sie beendet, da Wtsapi32.dll nicht vorhanden ist.

Informationen zum Bestimmen, ob Ihre Anwendung in einer Remotedesktopdienste-Umgebung ausgeführt wird, finden Sie unter [Detecting the Remotedesktopdienste Environment](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Programmierrichtlinien](general-programming-guidelines.md)
</dt> </dl>

 

 