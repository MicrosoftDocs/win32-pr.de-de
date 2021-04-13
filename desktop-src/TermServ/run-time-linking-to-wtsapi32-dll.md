---
title: Run-Time verknüpfen mit Wtsapi32.dll
description: Die Anwendung kann die Remotedesktopdienste-API verwenden, um zur Laufzeit dynamisch mit der Wtsapi32.dll zu verknüpfen. Zu diesem Zweck sollte die Anwendung die LoadLibrary-Funktion zum Laden Wtsapi32.dll abrufen.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390710"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time verknüpfen mit Wtsapi32.dll

Wenn Ihre Anwendung in einer Umgebung ausgeführt wird, die keine Remotedesktopdienste Umgebung ist, aber Sie möchten, dass Ihre Anwendung zusätzliche Funktionen bereitstellt, wenn Sie in einer Remotedesktopdienste Umgebung ausgeführt wird, kann die Anwendung die Remotedesktopdienste-API verwenden, um die zusätzlichen Funktionen zu implementieren, und zur Laufzeit dynamisch mit der Wtsapi32.dll verknüpfen. Zu diesem Zweck sollte die Anwendung die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion zum Laden Wtsapi32.dll abrufen. Wenn der **LoadLibrary** -Rückruf fehlschlägt, kann die Anwendung mit der grundlegenden Funktionalität ausgeführt werden. Wenn **LoadLibrary** erfolgreich ist, kann die Anwendung die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen, um Zeiger auf die Remotedesktopdienste Funktionen abzurufen, die Sie aufrufen möchten.

Wenn Ihre Anwendung nur für eine Remotedesktopdienste Umgebung vorgesehen ist, ist die dynamische Verknüpfung nicht erforderlich. In diesem Fall können Sie Wtsapi32. h einschließen und mit Wtsapi32. lib verknüpfen. Wenn Ihre Anwendung in einer anderen Umgebung als Remotedesktopdienste gestartet wird, wird Sie beendet, da Wtsapi32.dll nicht vorhanden ist.

Informationen zum bestimmen, ob Ihre Anwendung in einer Remotedesktopdienste-Umgebung ausgeführt wird, finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Programmier Richtlinien](general-programming-guidelines.md)
</dt> </dl>

 

 