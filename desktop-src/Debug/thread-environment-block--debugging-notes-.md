---
description: Thread Umgebungs Block (debugnotizen)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Thread Umgebungs Block (debugnotizen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861143"
---
# <a name="thread-environment-block-debugging-notes"></a>Thread Umgebungs Block (debugnotizen)

Der Thread Umgebungs Block ([**TEB-Struktur**](/windows/win32/api/winternl/ns-winternl-teb)) enthält Kontextinformationen für einen Thread.

In den folgenden Versionen von Windows beträgt der Offset der 32-Bit-TEB-Adresse innerhalb des 64-Bit-TEB 0. Dies kann für den direkten Zugriff auf das 32-Bit-TEB eines WOW64-Threads verwendet werden. Dies ändert sich möglicherweise in späteren Versionen von Windows.



|               |                        |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Strukturen](debugging-structures.md)
</dt> <dt>

[**WOW64- \_ Kontext**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
