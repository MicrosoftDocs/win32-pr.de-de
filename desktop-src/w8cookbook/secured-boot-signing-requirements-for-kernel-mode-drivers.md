---
title: Signierungsanforderungen für sichere Startfeatures für Kernelmodustreiber
description: Signierungsanforderungen für sichere Startfeatures für Kernelmodustreiber
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6593df6707dc26b36fceca796c436ed45f3f0c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885072"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Signierungsanforderungen für sichere Startfeatures für Kernelmodustreiber

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>Beschreibung

In Windows 8 und Windows Server 2012, einschließlich WinPE, wurde der Kernel gesperrt, um zu verhindern, dass durch Start- oder Stammkits eingeführte Schadsoftware Windows Sicherheitsanforderungen des Betriebssystems für signierte Treiber umgangen wird.

Diese Änderung wirkt sich auf alle Kernelmodustreiber für Geräte aus, die den sicheren Start der einheitlichen erweiterbaren Firmwareschnittstelle (UEFI) unterstützen. Der sichere UEFI-Start ist für Windows 8 Zertifizierung für Clientcomputer und optional für Server erforderlich. Sie wirkt sich nicht auf Benutzermodustreiber aus.

Die Standardentwicklung für Kernelmodustreiber umfasst entweder die Verwendung des Debuggens im Kernelmodus oder der Testsignierungseinstellung für Startkonfigurationsdaten (Boot Configuration Data, &lt; &gt; BCD). Beide sind deaktiviert, wenn der gesicherte Start aktiviert ist.

## <a name="manifestation"></a>Manifestation

Kernelmodustreiber werden nicht ausgeführt, wenn sie nicht ordnungsgemäß von einer vertrauenswürdigen Zertifizierungsstelle signiert wurden. Das Betriebssystem lässt die Ausführung nicht vertrauenswürdiger Treiber nicht zu, und Standardmechanismen wie Kerneldebuggen und Testsignierung sind nicht zulässig.

## <a name="mitigation"></a>Minderung

Zum Testen von Treibern müssen Sie den sicheren Start im BIOS deaktivieren und die anderen Testsignaturanforderungen erfüllen (siehe unten).

Bei einer umfassenderen Verteilung von Treibern müssen sie ordnungsgemäß von einer vertrauenswürdigen Zertifizierungsstelle signiert werden.

## <a name="resources"></a>Ressourcen

-   [Signieren von Treibern](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 
