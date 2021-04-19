---
title: Funktionen zum Signieren von sicheren Start Features für Kernelmodustreiber
description: Funktionen zum Signieren von sicheren Start Features für Kernelmodustreiber
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106342168"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Funktionen zum Signieren von sicheren Start Features für Kernelmodustreiber

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

In Windows 8 und Windows Server 2012, einschließlich WinPE, wurde der Kernel gesperrt, um zu verhindern, dass Schadsoftware, die von Start-oder Rootkits eingeführt wurde, die Sicherheitsanforderungen des Windows-Betriebssystems für signierte Treiber umgeht.

Diese Änderung wirkt sich auf alle Kernelmodustreiber für Geräte aus, die den sicheren Start von Unified Extensible Firmware Interface (UEFI) unterstützen. UEFI Secure Boot ist für die Windows 8-Zertifizierung für Client Computer und optional für-Server erforderlich. Er wirkt sich nicht auf Benutzermodus-Treiber aus.

Die Standard Entwicklung für Kernelmodustreiber umfasst entweder die Verwendung des kernelmodusdebuggens oder die Start Konfigurationsdaten-Einstellung (BCD) <testsigning> . Beide werden deaktiviert, wenn der sichere Start aktiviert ist.

## <a name="manifestation"></a>Ausstrahlung

Kernelmodustreiber können nicht ausgeführt werden, wenn Sie von einer vertrauenswürdigen Zertifizierungsstelle nicht ordnungsgemäß signiert wurden. Das Betriebssystem lässt nicht zu, dass nicht vertrauenswürdige Treiber ausgeführt werden, und Standardmechanismen wie Kernel Debugging und TESTSIGNING sind nicht zulässig.

## <a name="mitigation"></a>Minderung

Zum Testen von Treibern müssen Sie den sicheren Start im BIOS deaktivieren und die anderen Anforderungen an die Test Signierung erfüllen (siehe unten).

Wenn Treiber häufiger verteilt werden, müssen Sie von einer vertrauenswürdigen Zertifizierungsstelle ordnungsgemäß signiert werden.

## <a name="resources"></a>Ressourcen

-   [Signatur Treiber](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 