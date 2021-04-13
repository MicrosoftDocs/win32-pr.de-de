---
title: Kernel Überprüfungen für nicht-WHQL-signierte Treiber
description: Bei Geräten, die die Installation von Windows 10 bereinigen und bei denen der sichere Start auf ON fest steht (Beachten Sie, dass dies für alle neuen Geräte seit der Veröffentlichung von Windows 8,0 der Standard ist), müssen alle neuen Treiber von WHQL/sysdev signiert werden, anstatt nur Kreuz signierte Zertifikate zu verwenden.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388592"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Kernel Überprüfungen für nicht-WHQL-signierte Treiber

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Bei Geräten, die die Installation von Windows 10 bereinigen und bei denen der sichere Start auf ON fest steht (Beachten Sie, dass dies für alle neuen Geräte seit der Veröffentlichung von Windows 8,0 der Standard ist), müssen alle neuen Treiber von WHQL/sysdev signiert werden, anstatt nur Kreuz signierte Zertifikate zu verwenden. Geräte, für die ein Upgrade durchgeführt wurde, und Fälle, in denen Treiber mit einem Kreuz Zertifikat signiert wurden, bevor diese Richtlinie wirksam wird, werden von dieser Richtlinie ausgeschlossen, um die Abwärtskompatibilität sicherzustellen Diese Richtlinie wurde am 2015. April angekündigt, Sie wird jedoch mit der Windows Anniversary Edition (Version August 2016) erzwungen.

In Fällen, in denen ein Treiber nicht ordnungsgemäß signiert ist, wird er als PCA-Benachrichtigung angezeigt, dass die Treiber blockiert werden, wenn Sie die Signatur Anforderungen nicht bestehen. Dadurch wird verhindert, dass der Treiber, der nicht mehr im Kernel blockiert wird, transparent blockiert wird.

Weitere Informationen finden Sie in [diesem Blogbeitrag](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), in dem die Treiber Signier Änderung angekündigt wird.

 

 




