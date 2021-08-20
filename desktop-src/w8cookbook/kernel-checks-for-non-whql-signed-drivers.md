---
title: Kernelüberprüfungen für Nicht-WHQL-signierte Treiber
description: Für Geräte, die Windows 10 neu installieren und bei denen der sichere Start aktiviert ist (beachten Sie, dass dies seit der Veröffentlichung von Windows 8.0 standard ist), müssen alle neuen Treiber von WHQL/Sysdev signiert werden, anstatt nur kreuzsignierte Zertifikate zu verwenden.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810d0549086d36f146ca80c0b9c83a7258bb3b120202432cdab6203a081cdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852416"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Kernelüberprüfungen für Nicht-WHQL-signierte Treiber

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Für Geräte, die Windows 10 neu installieren und bei denen der sichere Start aktiviert ist (beachten Sie, dass dies seit der Veröffentlichung von Windows 8.0 standard ist), müssen alle neuen Treiber von WHQL/Sysdev signiert werden, anstatt nur kreuzsignierte Zertifikate zu verwenden. Geräte, für die ein Upgrade durchgeführt wird, und Fälle, in denen Treiber mit einem Kreuzzertifikat signiert wurden, bevor diese Richtlinie wirksam wurde, werden von dieser Richtlinie ausgeschlossen, um abwärtskompatibel zu sein. Diese Richtlinie wurde im April 2015 angekündigt. Sie wird jedoch mit der Windows Anniversary Edition erzwungen, die im August 2016 veröffentlicht wurde.

Wenn ein Treiber nicht ordnungsgemäß signiert ist, wird er als PCA-Benachrichtigung angezeigt, dass die Treiber blockiert werden, wenn er die Signaturanforderungen nicht erfüllt. Dadurch wird verhindert, dass die Benutzerfreundlichkeit des Treibers im Kernel später nicht mehr transparent ist.

Weitere Informationen finden Sie in [diesem Blogbeitrag,](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/)in dem die Änderung der Treibersignatur angekündigt wird.

 

 




