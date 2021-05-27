---
description: Threadumgebungsblock (Debughinweise)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Threadumgebungsblock (Debughinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550585"
---
# <a name="thread-environment-block-debugging-notes"></a>Threadumgebungsblock (Debughinweise)

Der Threadumgebungsblock [**(TEB-Struktur)**](/windows/win32/api/winternl/ns-winternl-teb)enthält Kontextinformationen für einen Thread.

In den folgenden Versionen von Windows ist der Offset der 32-Bit-TEB-Adresse innerhalb des 64-Bit-TEB 0. Dies kann verwendet werden, um direkt auf den 32-Bit-TEB eines WOW64-Threads zuzugreifen. Dies kann sich in späteren Versionen von Windows ändern.



|  Plattform     | Version                |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Strukturen](debugging-structures.md)
</dt> <dt>

[**\_WOW64-KONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
