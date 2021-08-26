---
title: Anforderungen an die Signierung sicherer Startfeatures für Kernelmodustreiber
description: Anforderungen an die Signierung sicherer Startfeatures für Kernelmodustreiber
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05146645e01406fed0129c4f31660509e04581ce889213c7addf01731e45e87f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932170"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Anforderungen an die Signierung sicherer Startfeatures für Kernelmodustreiber

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>Beschreibung

In Windows 8 und Windows Server 2012, einschließlich WinPE, wurde der Kernel gesperrt, um zu verhindern, dass schadsoftware, die durch Boot- oder Root Kits eingeführt wird, die Sicherheitsanforderungen des Windows-Betriebssystems für signierte Treiber umgehen kann.

Diese Änderung wirkt sich auf alle Kernelmodustreiber für Geräte aus, die den sicheren Start der einheitlichen erweiterbaren Firmwareschnittstelle (UEFI) unterstützen. Der sichere UEFI-Start ist für Windows 8-Zertifizierung für Clientcomputer und optional für Server erforderlich. Dies wirkt sich nicht auf Treiber im Benutzermodus aus.

Die Standardentwicklung für Kernelmodustreiber umfasst entweder das Debuggen im Kernelmodus oder die Einstellung für Startkonfigurationsdaten (Boot Configuration <testsigning> Data, BCD). Beides ist deaktiviert, wenn der gesicherte Start aktiviert ist.

## <a name="manifestation"></a>Manifestation

Treiber im Kernelmodus werden nicht ausgeführt, wenn sie nicht ordnungsgemäß von einer vertrauenswürdigen Zertifizierungsstelle signiert wurden. Das Betriebssystem lässt nicht vertrauenswürdige Treiber nicht zu, und Standardmechanismen wie Kerneldebuggen und Testsignierung sind nicht zulässig.

## <a name="mitigation"></a>Minderung

Zum Testen von Treibern müssen Sie den sicheren Start in BIOS deaktivieren und die anderen Testsignieranforderungen erfüllen (siehe unten).

Wenn Treiber häufiger verteilt werden, müssen sie ordnungsgemäß von einer vertrauenswürdigen Zertifizierungsstelle signiert werden.

## <a name="resources"></a>Ressourcen

-   [Signierungstreiber](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 